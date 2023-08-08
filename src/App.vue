<template>
  <Progressbar />
  <Header></Header>
  <Content><p>
      Aliquam faucibus quam lacus, eget facilisis purus luctus in. Nunc quis
      nunc faucibus, luctus risus vulputate, faucibus turpis. Phasellus lectus
      augue, vehicula at commodo sit amet, dictum eget sapien. Nulla sem turpis,
      bibendum quis malesuada in, hendrerit et nisl. Vestibulum odio sem,
      bibendum eu accumsan nec, sollicitudin pharetra sem. Vestibulum vestibulum
      volutpat massa. Etiam eu felis dapibus, fringilla urna ut, tempor lectus.
    </p>

    <p>
      Nunc nisl nulla, cursus sed ipsum sit amet, blandit rhoncus justo. In diam
      purus, hendrerit a pellentesque sed, dapibus nec metus. Nullam non congue
      est. Proin tempus enim et ipsum mollis eleifend eget eu turpis. Vestibulum
      pretium eget arcu sed pharetra. Cras vehicula euismod arcu laoreet tempus.
      Nam feugiat condimentum rutrum. Nunc nisi velit, aliquam nec ex fringilla,
      vehicula vehicula erat.
    </p></Content>
  <Carousel :images="[...images,...images]"></Carousel>
  <Content><p>
      Aliquam faucibus quam lacus, eget facilisis purus luctus in. Nunc quis
      nunc faucibus, luctus risus vulputate, faucibus turpis. Phasellus lectus
      augue, vehicula at commodo sit amet, dictum eget sapien. Nulla sem turpis,
      bibendum quis malesuada in, hendrerit et nisl. Vestibulum odio sem,
      bibendum eu accumsan nec, sollicitudin pharetra sem. Vestibulum vestibulum
      volutpat massa. Etiam eu felis dapibus, fringilla urna ut, tempor lectus.
    </p>

    <p>
      Nunc nisl nulla, cursus sed ipsum sit amet, blandit rhoncus justo. In diam
      purus, hendrerit a pellentesque sed, dapibus nec metus. Nullam non congue
      est. Proin tempus enim et ipsum mollis eleifend eget eu turpis. Vestibulum
      pretium eget arcu sed pharetra. Cras vehicula euismod arcu laoreet tempus.
      Nam feugiat condimentum rutrum. Nunc nisi velit, aliquam nec ex fringilla,
      vehicula vehicula erat.
    </p>
  </Content>

  <Reveal
    src="https://images.unsplash.com/photo-1536645152842-6b5fbacf1153?ixlib=rb-4.0.3&ixid=M3wxMjA3fDB8MHxwaG90by1wYWdlfHx8fGVufDB8fHx8fA%3D%3D&auto=format&fit=crop&w=1200&q=80"
    :type="RevealType.CENTER"
  />

  <Content><p>
      Aliquam faucibus quam lacus, eget facilisis purus luctus in. Nunc quis
      nunc faucibus, luctus risus vulputate, faucibus turpis. Phasellus lectus
      augue, vehicula at commodo sit amet, dictum eget sapien. Nulla sem turpis,
      bibendum quis malesuada in, hendrerit et nisl. Vestibulum odio sem,
      bibendum eu accumsan nec, sollicitudin pharetra sem. Vestibulum vestibulum
      volutpat massa. Etiam eu felis dapibus, fringilla urna ut, tempor lectus.
    </p>

    <Reveal
      src="https://images.unsplash.com/photo-1600758208050-a22f17dc5bb9?ixlib=rb-4.0.3&ixid=M3wxMjA3fDB8MHxwaG90by1wYWdlfHx8fGVufDB8fHx8fA%3D%3D&auto=format&fit=crop&w=1000&q=80"
      :type="RevealType.LEFT"
    />

    <p>
      Nunc nisl nulla, cursus sed ipsum sit amet, blandit rhoncus justo. In diam
      purus, hendrerit a pellentesque sed, dapibus nec metus. Nullam non congue
      est. Proin tempus enim et ipsum mollis eleifend eget eu turpis. Vestibulum
      pretium eget arcu sed pharetra. Cras vehicula euismod arcu laoreet tempus.
      Nam feugiat condimentum rutrum. Nunc nisi velit, aliquam nec ex fringilla,
      vehicula vehicula erat.
    </p></Content>  <Content><p>
      Aliquam faucibus quam lacus, eget facilisis purus luctus in. Nunc quis
      nunc faucibus, luctus risus vulputate, faucibus turpis. Phasellus lectus
      augue, vehicula at commodo sit amet, dictum eget sapien. Nulla sem turpis,
      bibendum quis malesuada in, hendrerit et nisl. Vestibulum odio sem,
      bibendum eu accumsan nec, sollicitudin pharetra sem. Vestibulum vestibulum
      volutpat massa. Etiam eu felis dapibus, fringilla urna ut, tempor lectus.
    </p>

    <p>
      Nunc nisl nulla, cursus sed ipsum sit amet, blandit rhoncus justo. In diam
      purus, hendrerit a pellentesque sed, dapibus nec metus. Nullam non congue
      est. Proin tempus enim et ipsum mollis eleifend eget eu turpis. Vestibulum
      pretium eget arcu sed pharetra. Cras vehicula euismod arcu laoreet tempus.
      Nam feugiat condimentum rutrum. Nunc nisi velit, aliquam nec ex fringilla,
      vehicula vehicula erat.
    </p>
    <p>
      Nunc nisl nulla, cursus sed ipsum sit amet, blandit rhoncus justo. In diam
      purus, hendrerit a pellentesque sed, dapibus nec metus. Nullam non congue
      est. Proin tempus enim et ipsum mollis eleifend eget eu turpis. Vestibulum
      pretium eget arcu sed pharetra. Cras vehicula euismod arcu laoreet tempus.
      Nam feugiat condimentum rutrum. Nunc nisi velit, aliquam nec ex fringilla,
      vehicula vehicula erat.
    </p>
  </Content> 
  <ImageList :images="images" />
  <Content>
      <p>
      Aliquam faucibus quam lacus, eget facilisis purus luctus in. Nunc quis
      nunc faucibus, luctus risus vulputate, faucibus turpis. Phasellus lectus
      augue, vehicula at commodo sit amet, dictum eget sapien. Nulla sem turpis,
      bibendum quis malesuada in, hendrerit et nisl. Vestibulum odio sem,
      bibendum eu accumsan nec, sollicitudin pharetra sem. Vestibulum vestibulum
      volutpat massa. Etiam eu felis dapibus, fringilla urna ut, tempor lectus.
    </p>

    <p>
      Nunc nisl nulla, cursus sed ipsum sit amet, blandit rhoncus justo. In diam
      purus, hendrerit a pellentesque sed, dapibus nec metus. Nullam non congue
      est. Proin tempus enim et ipsum mollis eleifend eget eu turpis. Vestibulum
      pretium eget arcu sed pharetra. Cras vehicula euismod arcu laoreet tempus.
      Nam feugiat condimentum rutrum. Nunc nisi velit, aliquam nec ex fringilla,
      vehicula vehicula erat.
    </p> 
    </Content>
    <Gallery intro="A gallery full of images, for you to see." :images="images" />
    <Content>
      <p>
      Aliquam faucibus quam lacus, eget facilisis purus luctus in. Nunc quis
      nunc faucibus, luctus risus vulputate, faucibus turpis. Phasellus lectus
      augue, vehicula at commodo sit amet, dictum eget sapien. Nulla sem turpis,
      bibendum quis malesuada in, hendrerit et nisl. Vestibulum odio sem,
      bibendum eu accumsan nec, sollicitudin pharetra sem. Vestibulum vestibulum
      volutpat massa. Etiam eu felis dapibus, fringilla urna ut, tempor lectus.
    </p>

    <p>
      Nunc nisl nulla, cursus sed ipsum sit amet, blandit rhoncus justo. In diam
      purus, hendrerit a pellentesque sed, dapibus nec metus. Nullam non congue
      est. Proin tempus enim et ipsum mollis eleifend eget eu turpis. Vestibulum
      pretium eget arcu sed pharetra. Cras vehicula euismod arcu laoreet tempus.
      Nam feugiat condimentum rutrum. Nunc nisi velit, aliquam nec ex fringilla,
      vehicula vehicula erat.
    </p>
  </Content>
    <Content>
      <p>
      Aliquam faucibus quam lacus, eget facilisis purus luctus in. Nunc quis
      nunc faucibus, luctus risus vulputate, faucibus turpis. Phasellus lectus
      augue, vehicula at commodo sit amet, dictum eget sapien. Nulla sem turpis,
      bibendum quis malesuada in, hendrerit et nisl. Vestibulum odio sem,
      bibendum eu accumsan nec, sollicitudin pharetra sem. Vestibulum vestibulum
      volutpat massa. Etiam eu felis dapibus, fringilla urna ut, tempor lectus.
    </p>

    <p>
      Nunc nisl nulla, cursus sed ipsum sit amet, blandit rhoncus justo. In diam
      purus, hendrerit a pellentesque sed, dapibus nec metus. Nullam non congue
      est. Proin tempus enim et ipsum mollis eleifend eget eu turpis. Vestibulum
      pretium eget arcu sed pharetra. Cras vehicula euismod arcu laoreet tempus.
      Nam feugiat condimentum rutrum. Nunc nisi velit, aliquam nec ex fringilla,
      vehicula vehicula erat.
    </p>
  </Content>

  <ImageColumns :images="[[images[0], images[1], images[2]], [images[2], images[3], images[4]], [images[4], images[5], images[1]]]" />
    <Content>
      <p>
      Aliquam faucibus quam lacus, eget facilisis purus luctus in. Nunc quis
      nunc faucibus, luctus risus vulputate, faucibus turpis. Phasellus lectus
      augue, vehicula at commodo sit amet, dictum eget sapien. Nulla sem turpis,
      bibendum quis malesuada in, hendrerit et nisl. Vestibulum odio sem,
      bibendum eu accumsan nec, sollicitudin pharetra sem. Vestibulum vestibulum
      volutpat massa. Etiam eu felis dapibus, fringilla urna ut, tempor lectus.
    </p>

    <p>
      Nunc nisl nulla, cursus sed ipsum sit amet, blandit rhoncus justo. In diam
      purus, hendrerit a pellentesque sed, dapibus nec metus. Nullam non congue
      est. Proin tempus enim et ipsum mollis eleifend eget eu turpis. Vestibulum
      pretium eget arcu sed pharetra. Cras vehicula euismod arcu laoreet tempus.
      Nam feugiat condimentum rutrum. Nunc nisi velit, aliquam nec ex fringilla,
      vehicula vehicula erat.
    </p>
  </Content>
    <Content>
      <p>
      Aliquam faucibus quam lacus, eget facilisis purus luctus in. Nunc quis
      nunc faucibus, luctus risus vulputate, faucibus turpis. Phasellus lectus
      augue, vehicula at commodo sit amet, dictum eget sapien. Nulla sem turpis,
      bibendum quis malesuada in, hendrerit et nisl. Vestibulum odio sem,
      bibendum eu accumsan nec, sollicitudin pharetra sem. Vestibulum vestibulum
      volutpat massa. Etiam eu felis dapibus, fringilla urna ut, tempor lectus.
    </p>

    <p>
      Nunc nisl nulla, cursus sed ipsum sit amet, blandit rhoncus justo. In diam
      purus, hendrerit a pellentesque sed, dapibus nec metus. Nullam non congue
      est. Proin tempus enim et ipsum mollis eleifend eget eu turpis. Vestibulum
      pretium eget arcu sed pharetra. Cras vehicula euismod arcu laoreet tempus.
      Nam feugiat condimentum rutrum. Nunc nisi velit, aliquam nec ex fringilla,
      vehicula vehicula erat.
    </p>
  </Content>
    <Content>
      <p>
      Aliquam faucibus quam lacus, eget facilisis purus luctus in. Nunc quis
      nunc faucibus, luctus risus vulputate, faucibus turpis. Phasellus lectus
      augue, vehicula at commodo sit amet, dictum eget sapien. Nulla sem turpis,
      bibendum quis malesuada in, hendrerit et nisl. Vestibulum odio sem,
      bibendum eu accumsan nec, sollicitudin pharetra sem. Vestibulum vestibulum
      volutpat massa. Etiam eu felis dapibus, fringilla urna ut, tempor lectus.
    </p>

    <p>
      Nunc nisl nulla, cursus sed ipsum sit amet, blandit rhoncus justo. In diam
      purus, hendrerit a pellentesque sed, dapibus nec metus. Nullam non congue
      est. Proin tempus enim et ipsum mollis eleifend eget eu turpis. Vestibulum
      pretium eget arcu sed pharetra. Cras vehicula euismod arcu laoreet tempus.
      Nam feugiat condimentum rutrum. Nunc nisi velit, aliquam nec ex fringilla,
      vehicula vehicula erat.
    </p>
  </Content>
    <Content>
      <p>
      Aliquam faucibus quam lacus, eget facilisis purus luctus in. Nunc quis
      nunc faucibus, luctus risus vulputate, faucibus turpis. Phasellus lectus
      augue, vehicula at commodo sit amet, dictum eget sapien. Nulla sem turpis,
      bibendum quis malesuada in, hendrerit et nisl. Vestibulum odio sem,
      bibendum eu accumsan nec, sollicitudin pharetra sem. Vestibulum vestibulum
      volutpat massa. Etiam eu felis dapibus, fringilla urna ut, tempor lectus.
    </p>

    <p>
      Nunc nisl nulla, cursus sed ipsum sit amet, blandit rhoncus justo. In diam
      purus, hendrerit a pellentesque sed, dapibus nec metus. Nullam non congue
      est. Proin tempus enim et ipsum mollis eleifend eget eu turpis. Vestibulum
      pretium eget arcu sed pharetra. Cras vehicula euismod arcu laoreet tempus.
      Nam feugiat condimentum rutrum. Nunc nisi velit, aliquam nec ex fringilla,
      vehicula vehicula erat.
    </p>
  </Content>
</template>

<script setup lang="ts">
import Progressbar from "./components/Progressbar.vue";
import Header from "./components/Header.vue";
import Content from "./components/Content.vue";
import Carousel from "./components/Carousel.vue";
import Gallery from "./components/Gallery.vue";
import Reveal from "./components/Reveal.vue";
import { RevealType } from "./components/Reveal.model";
import ImageList from "./components/ImageList.vue";
import ImageColumns from "./components/ImageColumns.vue";

const images = [
  {
    src: "https://images.unsplash.com/photo-1583610261946-5d88e555be93?ixlib=rb-4.0.3&ixid=M3wxMjA3fDB8MHxwaG90by1wYWdlfHx8fGVufDB8fHx8fA%3D%3D&auto=format&fit=crop&w=720&q=80",
  },
  {
    src: "https://images.unsplash.com/photo-1567960095052-d15f59a1a309?ixlib=rb-4.0.3&ixid=M3wxMjA3fDB8MHxwaG90by1wYWdlfHx8fGVufDB8fHx8fA%3D%3D&auto=format&fit=crop&w=720&q=80",
  },
  {
    src: "https://images.unsplash.com/photo-1620982591827-5e003e8d26fb?ixlib=rb-4.0.3&ixid=M3wxMjA3fDB8MHxwaG90by1wYWdlfHx8fGVufDB8fHx8fA%3D%3D&auto=format&fit=crop&w=720&q=80",
  },
  {
    src: "https://images.unsplash.com/photo-1598897270268-f7091c801c3d?ixlib=rb-4.0.3&ixid=M3wxMjA3fDB8MHxwaG90by1wYWdlfHx8fGVufDB8fHx8fA%3D%3D&auto=format&fit=crop&w=720&q=80",
  },
  {
    src: "https://images.unsplash.com/photo-1609931552570-9056ce113c77?ixlib=rb-4.0.3&ixid=M3wxMjA3fDB8MHxwaG90by1wYWdlfHx8fGVufDB8fHx8fA%3D%3D&auto=format&fit=crop&w=720&q=80",
  },
  {
    src: "https://images.unsplash.com/photo-1557600032-8ebbe06dc226?ixlib=rb-4.0.3&ixid=M3wxMjA3fDB8MHxwaG90by1wYWdlfHx8fGVufDB8fHx8fA%3D%3D&auto=format&fit=crop&w=720&q=80",
  }
];
</script>

<style scoped></style>
