<template lang="pug">
  .contact
    section#contact.bg-white.py-5
      .container
        .row
          .col-12
            .title
              h3 Contact
              span Contact me to learn how we can work together
        .row
          .col-xl-4.mb-5.mb-xl-0
            h4.mb-3 Get in touch
            p.mb-4 Feel free to reach out to me to discuss projects you have or are interested in.  I'm available at the info below or you can use the contact form.
            .row.mb-3
              .col-6
                strong Email
              .col-6.text-nowrap mark [-at-] aroach.com
            .row.mb-3
              .col-6
                strong Phone
              .col-6.text-nowrap (713) 876-1547
            .row
              .col-6
                strong LinkedIn
              .col-6
                a(href="https://www.linkedin.com/in/roachm/", target="_blank") Visit
          .col-xl-6.offset-xl-2
            form
              .form-row
                .form-group.col-lg-6
                  //label Name
                  input.form-control(type="text", placeholder="Name")
                .form-group.col-lg-6
                  //label E-mail
                  input.form-control(type="email", placeholder="E-mail address")
              .form-row
                .form-group.col-12
                  //label Message
                  textarea.form-control(rows="5", placeholder="Enter a message to send")
              .form-row
                .col-12
                  button.btn.btn-primary Send Message
</template>
