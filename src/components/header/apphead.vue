<template>
  <div class="appheader">
    <div>
      <h1>Free Unlimited Web Hosting</h1>
      <p>Completely free website hosting with unlimited disk space and bandwidth.</p>
      <btn
        href="#learnmore"
        value="Learn More"
        styl="
            grid-area: learnmore;
            border-radius: 10px 0px 0px 10px;
            margin-left: 10px;
          "
      />
      <btn
        href="#signup"
        value="SignUp"
        styl="
          grid-area: signup;
          border-radius: 0px 10px 10px 0px;
          margin-right: 10px;
        "
        />
    </div>
  </div>
</template>

<script>
import btn from './btn';
export default {
  name: 'appheader',
  components: {
    btn
  }
}
</script>

<style>
    .appheader {
        background: url("/header.jpg");
        background-size: cover;
        display: grid;
    }
    .appheader > div {
        color: black;
        background: aliceblue;
        opacity: 0.6;
        border-top: 1px dotted black;
        border-bottom: 2px dotted black;
        display: grid;
        grid-template-columns: repeat(4, 1fr);
        grid-template-rows: repeat(8, auto);
        grid-template-areas:
            ". . . ."
            ". . . ."
            ". . . ."
            "heading heading heading heading"
            "subheading subheading subheading subheading"
            ". learnmore signup ."
            ". . . ."
            ". . . .";
    }
    .appheader > div > h1 {
        text-align: center;
        grid-area: heading;
        background: #ffffff;
        opacity: 4;
    }
    .appheader > div > p {
        font-size: 16px;
        text-align: center;
        grid-area: subheading;
        background: #ffffff;
        opacity: 1;
    }
    @media only screen and (max-width: 700px){
      .appheader > div{
        grid-template-columns: 1fr 1fr;
        grid-template-areas: 
          ". ."
          ". ."
          ". ."
          "heading heading"
          "subheading subheading"
          "learnmore signup"
          ". ."
          ". .";
      }
    }
</style>
