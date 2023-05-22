---
title: ""
permalink: /
date: 2021-05-06
layout: archive
classes: wide

# Tutorials
feature_row:
- image_path: /files/DLPOIcon.JPG
  alt: ""
  title: "DL + PO"
  excerpt: "Building deep learning estimators for causal inference. Gentle intro to Tensorflow 2."
  url: "https://github.com/kochbj/Deep-Learning-for-Causal-Inference"
- image_path: /files/White-Square.jpg
- image_path: /files/LiteRateIcon.png
  title: "LiteRate"
  excerpt: "Studying change in (cultural, organizational, human) populations through birth/death rates."
  url: "https://github.com/dsilvestro/LiteRate"

---
# Hello!
I'm Bernie. You can check out my résumé/CV to learn a bit about me. I'm mostly using this site to share things I've been working on. Feel free to reach out if you'd like to chat!



**02/23/2023:** I have updated my [Deep Learning for Causal Inference](https://github.com/kochbj/Deep-Learning-for-Causal-Inference) tutorial series with a new tutorial on uncertainty and interpretation.
{: .notice}

**02/18/2023:** Excited to do a postdoc at Northwestern's Kellogg School of Management with Dashun Wang!
{: .notice}

**01/24/2023:** I'm delighted to be joining the faculty at UChicago Sociology! 
{: .notice}

**03/22/2022:** I'm excited to be interning at Spotify Tech Research this summer.
{: .notice}

**03/22/2022:** Jacob Foster and I were invited to speak at Apple University about "[Reduced, Reused, and Recycled: The Life of a Benchmark in Machine Learning Research](https://openreview.net/forum?id=zNQBIBKJRkd)".
{: .notice}

**01/01/2022:** I am teaching an "Intro to Computational Social Science" course at Colby College for a month. After living in SoCal so long, I'm looking forward to the snow!
{: .notice}

**11/30/2021:** "[Reduced, Reused, and Recycled: The Life of a Benchmark in Machine Learning Research](https://openreview.net/forum?id=zNQBIBKJRkd)" with Emily Denton, Alex Hanna, and my advisor Jacob Foster won an award for ["Best Paper"](https://blog.neurips.cc/2021/11/30/announcing-the-neurips-2021-award-recipients/?s=09) in the Datasets and Benchmarks Track at NeurIPS 2021. This was one of nine paper awards given at the whole conference. I'm frankly shocked (and delighted) that it resonated so strongly with people!
{: .notice}

**10/5/2021:** "[Reduced, Reused, and Recycled: The Life of a Benchmark in Machine Learning Research](https://openreview.net/forum?id=zNQBIBKJRkd)" with Emily Denton, Alex Hanna, and my advisor Jacob Foster was accepted as an oral presentation at NeurIPS 2021.
{: .notice}

**08/1/2021:** The NSF Science of Science program gave me a DDRIG grant to do my dissertation.
{: .notice}
  
### Tutorials
{% include feature_row %}

{::nomarkdown}

.cd-timeline {
  overflow: hidden;
  padding: var(--space-lg) 0;
}

.cd-timeline__container {
  position: relative;
  padding: var(--space-md) 0;

  &::before { // this is the timeline vertical line
    content: '';
    position: absolute;
    top: 0;
    left: 18px;
    height: 100%;
    width: 4px;
    background: var(--cd-color-2);
  }
}
.cd-timeline__block {
  display: flex;

  @include breakpoint(md) {
    &:nth-child(even) {
      flex-direction: row-reverse; // for even blocks -> lay out content from right to left
    }
  }
}

.cd-timeline__img {
  display: flex;
  justify-content: center;
  align-items: center;
  flex-shrink: 0;

  @include breakpoint(md) {
      order: 1; // flex order -> place the image after cd-timeline__content
   }
}

.cd-timeline__content {
   flex-grow: 1; // expand element so that it takes up all the available space inside its parent

   @include breakpoint(md) {
      width: 45%;
      flex-grow: 0; // prevent element from growing inside its parent
   }
}

@include breakpoint(md) { // animations
  .cd-timeline__img--hidden, .cd-timeline__content--hidden {
    visibility: hidden;
  }

  .cd-timeline__img--bounce-in {
    animation: cd-bounce-1 0.6s;
  }
}

@keyframes cd-bounce-1 {
  0% {
    opacity: 0;
    transform: scale(0.5);
  }
  60% {
    opacity: 1;
    transform: scale(1.2);
  }
  100% {
    transform: scale(1);    
  }
}
function VerticalTimeline( element ) {
   this.element = element;
   this.blocks = this.element.getElementsByClassName("cd-timeline__block");
   this.images = this.element.getElementsByClassName("cd-timeline__img");
   this.contents = this.element.getElementsByClassName("cd-timeline__content");
   // ..
};

VerticalTimeline.prototype.showBlocks = function() {
   var self = this;
   for( var i = 0; i < this.blocks.length; i++) {
      (function(i){
         if( self.contents[i].classList.contains("cd-timeline__content--hidden") && self.blocks[i].getBoundingClientRect().top <= window.innerHeight*self.offset ) {
            // add bounce-in animation
            self.images[i].classList.add("cd-timeline__img--bounce-in");
            self.contents[i].classList.add("cd-timeline__content--bounce-in");
            self.images[i].classList.remove("cd-timeline__img--hidden");
            self.contents[i].classList.remove("cd-timeline__content--hidden");
         }
      })(i);
   }
};

<section class="cd-timeline js-cd-timeline">
  <div class="container max-width-lg cd-timeline__container">
    <div class="cd-timeline__block">
      <div class="cd-timeline__img cd-timeline__img--picture">
        <img src="assets/img/cd-icon-picture.svg" alt="Picture">
      </div> <!-- cd-timeline__img -->

      <div class="cd-timeline__content text-component">
        <h2>Title of section 1</h2>
        <p class="color-contrast-medium">Lorem ipsum dolor sit amet, consectetur adipisicing elit. Iusto, optio, dolorum provident rerum aut hic quasi placeat iure tempora laudantium ipsa ad debitis unde? Iste voluptatibus minus veritatis qui ut.</p>

        <div class="flex justify-between items-center">
          <span class="cd-timeline__date">Jan 14</span>
          <a href="#0" class="btn btn--subtle">Read more</a>
        </div>
      </div> <!-- cd-timeline__content -->
    </div> <!-- cd-timeline__block -->

    <div class="cd-timeline__block">
      <!-- ... -->
    </div> <!-- cd-timeline__block -->
  </div>
</section> <!-- cd-timeline -->

{:/}
