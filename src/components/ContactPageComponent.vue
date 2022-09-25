<template lang="">
  <div>
    <section class="contact-page-sec container text-center">
      <h1 class="display-4">Contact <span style="color: #73caef">Us</span></h1>
      <div class="container">
        <div class="row">
          <div class="col-md-4">
            <div class="contact-info">
              <div class="contact-info-item">
                <div class="contact-info-icon">
                  <i class="fas fa-map-marked"></i>
                </div>
                <div class="contact-info-text">
                  <h3>address</h3>
                  <span
                    >80 Campground rondebosch</span
                  >
                  <span>Cape Town, South Africa</span>
                </div>
              </div>
            </div>
          </div>
          <div class="col-md-4">
            <div class="contact-info">
              <div class="contact-info-item">
                <div class="contact-info-icon">
                  <i class="fas fa-envelope"></i>
                </div>
                <div class="contact-info-text">
                  <h3>E-mail</h3>
                  <span> tshimsmarco@gmail.com</span>
                  <span>(+27) 727408325</span>
                  <span></span>
                </div>
              </div>
            </div>
          </div>
          <div class="col-md-4">
            <div class="contact-info">
              <div class="contact-info-item">
                <div class="contact-info-icon">
                  <i class="fas fa-clock"></i>
                </div>
                <div class="contact-info-text">
                  <h3>office time</h3>
                  <span>Mon - Fri 9:00 am - 5:00 pm</span>
                  <span>Suturday 10:00 am - 2:00 pm</span>
                  <span>Sunday closed</span>
                </div>
              </div>
            </div>
          </div>
        </div>
        <div class="row">
          <div class="col-md-8">
            <div class="contact-page-form">
              <h3 class="mb-3">Get in Touch</h3>
              <span class="alert alert-success mt-3" v-if="success">
                Message sent succefully !!
              </span>
              <form ref="form" @submit.prevent="handleSubmit">
                <div class="row">
                  <div class="col-md-6 col-sm-6 col-xs-12">
                    <div class="single-input-field">
                      <input
                        class="border"
                        v-model="$v.name.$model"
                        type="text"
                        placeholder="Your Name"
                        :class="{ 'is-invalid': $v.name.$error }"
                        name="name"
                      />
                      <div v-if="$v.name.$error" class="invalid-feedback">
                        <span v-if="!$v.name.required">name is required</span>
                      </div>
                    </div>
                  </div>
                  <div class="col-md-6 col-sm-6 col-xs-12">
                    <div class="single-input-field">
                      <input
                        class="border"
                        v-model="$v.email.$model"
                        type="email"
                        placeholder="E-mail"
                        :class="{ 'is-invalid': $v.email.$error }"
                        name="email"
                        required
                      />
                      <div v-if="$v.email.$error" class="invalid-feedback">
                        <span v-if="!$v.email.required">Email is required</span>
                        <span v-if="!$v.email.email">Email is invalid</span>
                      </div>
                    </div>
                  </div>
                  <div class="col-md-6 col-sm-6 col-xs-12">
                    <div class="single-input-field">
                      <input
                        class="border"
                        v-model="$v.phone.$model"
                        type="text"
                        placeholder="Phone Number"
                        :class="{ 'is-invalid': $v.phone.$error }"
                        name="phone"
                      />
                      <div v-if="$v.phone.$error" class="invalid-feedback">
                        <span v-if="!$v.phone.required"
                          >phone number is required</span
                        >
                        <span v-if="!$v.phone.minLength"
                          >phone number min length is 10</span
                        >
                        <span v-if="!$v.phone.maxLength"
                          >phone number max length is 10</span
                        >
                      </div>
                    </div>
                  </div>
         
           
                  <button
                    class="float-left mt-2 btn btn-danger"
                    type="submit"
                  >
                    send <b-spinner small v-if="isLoading"></b-spinner>
                  </button>
                </div>

                <span class="alert alert-danger" v-if="error"
                  >there is an error !!</span
                >
              </form>
            </div>
          </div>
          <div class="col-md-4">
            <div class="contact-page-map">
              <iframe
                src="https://www.google.com/maps/embed?pb=!1m18!1m12!1m3!1d13243.402788471383!2d18.4250213173703!3d-33.91924200915353!2m3!1f0!2f0!3f0!3m2!1i1024!2i768!4f13.1!3m3!1m2!1s0x1dcc6761a2419367%3A0x3f1d61e79628bf94!2s8%20Hans%20Strijdom%20Ave%2C%20Cape%20Town%20City%20Centre%2C%20Cape%20Town%2C%208000!5e0!3m2!1sen!2sza!4v1643832089770!5m2!1sen!2sza"
                height="450"
                style="border: 0"
                allowfullscreen=""
                loading="lazy"
              ></iframe>
            </div>
          </div>
        </div>
      </div>
    </section>
  </div>
</template>
<script>
import {
  required,
  email,
  minLength,
  maxLength,
} from "vuelidate/lib/validators";
import axios from "axios"

export default {
  data() {
    return {
      name: "",
      email: "",
      phone: "",
      success: false,
      error: false,
      isLoading: false,
    };
  },
  validations: {
    name: {
      required,
      minLength: minLength(3),
    },
    email: {
      required,
      email,
    },
    phone: {
      required,
      minLength: minLength(10),
      maxLength: maxLength(10),
    }

  },

  methods: {
    handleSubmit() {
        this.submitStatus = true;
        this.submitted = true;
        this.$v.$touch();
        if (this.$v.$invalid) {
          return;
        }
        this.message = "";
        this.errors = "";
        let formData = {
          name: this.name,
          email: this.email,
          phone: this.phone,

        };
          axios
            .post("http://dev3.elemental.co.za/elemental-cms/front_end/contact_form_test", formData)
            .then((res) => {
              (this.success = true), (this.submitted = false);
              this.message = res;
              console.log(this.message)
          
            })
            .catch((error) => {
              if (error.response.status == 422) {
                co
                this.success = false;
                this.errors = error.response.data;
                this.errors = error.response.data;
              }
             
            })
            .finally(() => {
              // this.message=null;
              this.submitStatus = false;
            });
      },
    },
};
</script>
<style>
.contact-image {
  height: 170px;
  width: 100%;
  background-size: cover;
}
section {
  padding: 60px 0;
  min-height: 80vh;
}
.contact-info {
  display: inline-block;
  width: 100%;
  text-align: center;
  margin-bottom: 10px;
}
.contact-info-icon {
  margin-bottom: 15px;
}
.contact-info-item {
  background: #071c34;
  padding: 30px 0px;
}
.contact-page-sec .contact-page-form h3 {
  color: #071c34;
  text-transform: capitalize;
  font-size: 22px;
  font-weight: 700;
}
.contact-page-form .col-md-6.col-sm-6.col-xs-12 {
  padding-left: 0;
}
.contact-page-form.contact-form input {
  margin-bottom: 5px;
}
.contact-page-form.contact-form textarea {
  height: 110px;
}
.contact-page-form.contact-form input[type="submit"] {
  background: #071c34;
  width: 150px;
  border-color: #071c34;
}
.contact-info-icon i {
  font-size: 48px;
  color: #fda40b;
}
.contact-info-text p {
  margin-bottom: 0px;
}
.contact-info-text h3 {
  color: #fff;
  font-size: 22px;
  text-transform: capitalize;
  font-weight: 600;
  margin-bottom: 10px;
}
.contact-info-text span {
  color: #999999;
  font-size: 16px;

  display: inline-block;
  width: 100%;
}

.contact-page-form input {
  background: #f9f9f9 none repeat scroll 0 0;
  border: 1px solid #f9f9f9;
  margin-bottom: 20px;
  padding: 12px 16px;
  width: 100%;
  border-radius: 4px;
}

.contact-page-form .message-input {
  display: inline-block;
  width: 100%;
  padding-left: 0;
}
.single-input-field textarea {
  background: #f9f9f9 none repeat scroll 0 0;
  border: 1px solid #f9f9f9;
  width: 100%;
  height: 120px;
  padding: 12px 16px;
  border-radius: 4px;
}
.single-input-fieldsbtn input[type="submit"] {
  background: #fda40b none repeat scroll 0 0;
  color: #fff;
  display: inline-block;
  font-weight: 600;
  padding: 10px 0;
  text-transform: capitalize;
  width: 150px;
  margin-top: 20px;
  font-size: 16px;
}
.single-input-fieldsbtn input[type="submit"]:hover {
  background: #071c34;
  transition: all 0.4s ease-in-out 0s;
  border-color: #071c34;
}
.single-input-field h4 {
  color: #464646;
  text-transform: capitalize;
  font-size: 14px;
}
.contact-page-form {
  display: inline-block;
  width: 100%;
  margin-top: 30px;
}

.contact-page-map {
  margin-top: 36px;
}
.contact-page-form form {
  padding: 20px 15px 0;
}
</style>
