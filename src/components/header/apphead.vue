<template>
  <div class="appheader">
    <div>
      <h1>Free Unlimited Web Hosting</h1>
      <p>Completely free web hosting with unlimited disk space and bandwidth.<br/>Just click <b>signup</b> button to get started.</p>
      <btn
        href="#learnmore"
        value="Learn More"
        styl="
            grid-area: learnmore;
            border-radius: 7px 0px 0px 7px;
            margin-left: 10px;
          "
      />
      <btn
        href="#signup"
        value="Signup Now"
        styl="
          grid-area: signup;
          border-radius: 0px 7px 7px 0px;
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
        background-position: center;
        display: grid;
        scroll-snap-align: start;
    }
    .appheader > div {
        color: #0c2246;
        background: aliceblue;
        opacity: 0.8;
        border-top: 3px dotted #0c2246;
        border-bottom: 3px dotted #0c2246;
        display: grid;
        grid-template-columns: repeat(4, 1fr);
        grid-template-rows: repeat(5, auto) 40px repeat(2, auto);
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
    }
    .appheader > div > p {
        font-size: 16px;
        text-align: center;
        grid-area: subheading;
    }
    @media only screen and (max-width: 700px){
      .appheader {
        background-size: cover;
        background-position: center;
      }
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
