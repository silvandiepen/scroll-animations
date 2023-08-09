<template>
  <Progressbar />
  <Header>
    Armenia <span>A Land of Rich History, Culture, and Resilience</span>
  </Header>
  <Content
    ><p>
      Nestled in the rugged Caucasus Mountains, Armenia stands as a testament to
      the power of human resilience, boasting a history that stretches back
      millennia and a culture that has endured through triumphs and
      tribulations. From its ancient roots to its modern challenges and
      accomplishments, Armenia is a nation that captivates with its unique blend
      of history, culture, and spirit.
    </p>
  </Content>
  <Carousel :images="[...images, ...images]"></Carousel>
  <Content>
    <h2>Historical Tapestry</h2>
    <p>
      Armenia's history is one of the oldest and most captivating in the world.
      The land that is modern-day Armenia has been inhabited since prehistoric
      times, with evidence of human presence dating back to the Paleolithic era.
      This region has played host to various civilizations, each leaving its
      mark on the land and its people.
    </p>
    <p>
      One of the most defining periods in Armenian history is the adoption of
      Christianity in the early 4th century, becoming the first nation to do so.
      This event, often attributed to the efforts of Saint Gregory the
      Illuminator, profoundly shaped the cultural and spiritual fabric of
      Armenia. Christianity not only influenced the nation's religious practices
      but also left a lasting impact on its art, architecture, and literature.
    </p>
    <p>
      Throughout the centuries, Armenia experienced both moments of greatness
      and periods of upheaval. The medieval Armenian Kingdom of Cilicia,
      situated in what is now modern-day Turkey, flourished as a center of
      commerce, learning, and artistic expression. However, the Armenian people
      also faced invasions, conflicts, and the tragic events of the Armenian
      Genocide during World War I, where an estimated 1.5 million Armenians lost
      their lives at the hands of the Ottoman Empire.
    </p>
  </Content>

  <Reveal
    src="https://images.unsplash.com/photo-1536645152842-6b5fbacf1153?ixlib=rb-4.0.3&ixid=M3wxMjA3fDB8MHxwaG90by1wYWdlfHx8fGVufDB8fHx8fA%3D%3D&auto=format&fit=crop&w=1200&q=80"
    :type="RevealType.CENTER"
  />

  <Content>
    <h2>Cultural Resilience</h2>

    <p>
      Armenia's culture is a mosaic woven from threads of history, religion, and
      artistic expression. The nation's literature, music, dance, and visual
      arts reflect its deep-rooted heritage and ability to endure adversity. The
      Armenian language, an Indo-European tongue with its own unique script, has
      been a cornerstone of the nation's identity, helping to preserve its
      cultural distinctiveness.
    </p>
    <p>
      <strong>Literature and Poetry:</strong> Armenian literature has a rich
      tradition that dates back centuries. One of the most notable figures in
      Armenian literature is the medieval poet and musician, Sayat-Nova, whose
      verses capture the beauty, pain, and love of his time. His work resonates
      to this day, serving as a testament to the enduring power of the written
      word.
    </p>
    <p>
      <strong>Art and Architecture:</strong> Armenian architecture is a blend of
      diverse influences, ranging from the pre-Christian era to the medieval
      period and beyond. The iconic Armenian Apostolic churches, characterized
      by their distinctive dome structures and intricate stone carvings, are not
      only places of worship but also living testaments to the craftsmanship of
      generations. Notable examples include the Etchmiadzin Cathedral,
      considered the oldest cathedral in the world, and the medieval monasteries
      of Haghpat and Sanahin.
    </p>
    <p>
      <strong>Music and Dance:</strong> Traditional Armenian music is deeply
      rooted in folklore and emotion. The duduk, an ancient double-reed woodwind
      instrument, produces haunting melodies that evoke a sense of melancholy
      and longing. Armenian folk dances, such as the Kochari and Shalakho,
      celebrate the joy of life and the spirit of unity.
    </p>

    <Reveal
      src="https://images.unsplash.com/photo-1600758208050-a22f17dc5bb9?ixlib=rb-4.0.3&ixid=M3wxMjA3fDB8MHxwaG90by1wYWdlfHx8fGVufDB8fHx8fA%3D%3D&auto=format&fit=crop&w=1000&q=80"
      :type="RevealType.LEFT"
    />

    <h2>Challenges and Triumphs</h2>
    <p>
      Armenia's history is marked by both its remarkable achievements and its
      challenges. In the modern era, the nation has navigated the complexities
      of post-Soviet independence and geopolitical pressures. The 1988
      earthquake in Spitak devastated parts of Armenia, claiming tens of
      thousands of lives and causing widespread destruction. The country's
      response to this tragedy highlighted its resilience and the global support
      it garnered.
    </p>

    <p>
      Another significant challenge has been the conflict with Azerbaijan over
      the Nagorno-Karabakh region. This conflict, rooted in historical and
      territorial disputes, culminated in a series of violent clashes, most
      notably in the early 1990s and, more recently, in 2020. The Armenian
      people's steadfastness in the face of adversity and their commitment to
      defending their cultural heritage on these battlegrounds serve as a
      testament to their enduring spirit.
    </p>
  </Content>
  <ImageList :images="images" />
  <Content>
    <h2>Cultural Heritage and Diaspora</h2>
    <p>
      The Armenian diaspora, spread across the globe, is a testament to the
      nation's ability to maintain its identity beyond its borders. Communities
      in countries such as the United States, France, Russia, and Lebanon have
      kept Armenian traditions alive through cultural events, religious
      practices, and educational initiatives. This diaspora plays a crucial role
      in preserving the language, culture, and history of Armenia, fostering a
      sense of belonging and unity among Armenians worldwide.
    </p>
</Content>

  <Gallery intro="A gallery full of images, for you to see." :images="images" />
  <Content>
    <h2>Modern Armenia</h2>
    <p>
      In recent years, Armenia has made strides in various sectors, including
      technology, agriculture, and tourism. The capital city, Yerevan, has
      evolved into a vibrant hub of culture and innovation, with its bustling
      streets, modern architecture, and thriving arts scene. The country's tech
      industry, often referred to as the "Silicon Mountains," has gained
      international recognition for its growth and innovation.
    </p>
    <p>
      Tourism in Armenia has been on the rise as well, drawing visitors to its
      historical sites, stunning landscapes, and warm hospitality. The medieval
      monasteries of Geghard and Tatev, perched on cliff sides and surrounded by
      breathtaking scenery, attract travelers and pilgrims alike. The serene
      waters of Lake Sevan, known as the "Jewel of Armenia," offer a tranquil
      retreat for both locals and visitors.
    </p></Content>

  <ImageColumns
    :images="[
      [images[0], images[1], images[2]],
      [images[2], images[3], images[4]],
      [images[4], images[5], images[1]],
    ]"
  />
  
  <Content>
    
    </Content>

<Content dark>
  <h2>Embracing Armenia: A Land of Endless Wonders and Unforgettable Experiences</h2>

<p>As we reflect on the remarkable journey of Armenia, it becomes abundantly clear that this nation is a gem that deserves to be cherished, explored, and celebrated. What sets Armenia apart and makes it an exceptional destination is not just its awe-inspiring landscapes, rich history, and enduring culture, but also the warmth of its people and the profound sense of connection one feels when stepping foot on its soil. Here's why Armenia stands as a great destination and an experience like no other.</p>

<h3>A Tapestry of Heritage and Culture</h3>

<p>Armenia's history is not merely confined to the pages of textbooks; it lives and breathes within its ancient churches, medieval monasteries, and intricately carved stone structures. The nation's commitment to preserving its cultural heritage has transformed these sites into living windows to the past, allowing visitors to immerse themselves in the stories of generations that came before. Whether exploring the haunting melodies of the duduk, marvelling at the architectural splendor of the Etchmiadzin Cathedral, or joining in the exuberant rhythms of Armenian folk dances, the cultural richness of Armenia is an experience that resonates deep within the soul.</p>

<h3>Landscapes of Unsurpassed Beauty</h3>

<p>Armenia's landscapes are as diverse as they are breathtaking. From the serene shores of Lake Sevan to the rugged peaks of Mount Ararat, the country's natural beauty captivates the senses and offers a serene escape from the hustle and bustle of modern life. The opportunity to explore the lush forests, tranquil valleys, and picturesque villages allows travelers to reconnect with nature and find solace in its embrace. The stark contrast between the tranquility of Lake Sevan and the grandeur of the ancient monasteries perched upon rocky cliffs creates a sense of wonder that lingers long after departure.</p>

<h3>Heartfelt Hospitality</h3>

<p>The people of Armenia are renowned for their warmth and genuine hospitality. Visitors are often welcomed with open arms, invited to share in traditional meals and stories that offer a glimpse into daily life and the traditions that bind this nation together. Whether savoring the flavors of Armenian cuisine, crafted with love and pride, or engaging in conversations that bridge cultural gaps, the hospitality of Armenia's people fosters connections that transcend borders.</p>

<h3>An Invitation to the Future</h3>

<p>Armenia's trajectory into the future is marked by innovation and progress. The Silicon Mountains have become a hub for technology and creativity, welcoming those with an appetite for the cutting edge. This juxtaposition of ancient history and modern innovation creates an environment where the past and future seamlessly coexist, inviting travelers to witness the evolution of a nation while preserving its timeless essence.</p>

<h3>The Call to Wander</h3>

<p>As the sun sets over the mountainous horizon of Armenia, a deep sense of gratitude and wonder settles upon those fortunate enough to have experienced its magic. Armenia beckons travelers not only to discover its history and culture but also to find a piece of themselves in the process. The landscapes, the people, the traditions—all come together to create an invitation to wander, to explore, and to connect.</p>

<p>So, why should you visit Armenia? The answer lies in the unparalleled fusion of past and present, the breathtaking landscapes, the vibrant culture, and the genuine connections that await. Armenia is more than a destination; it is an odyssey of the senses, an immersion into the soul of a nation that has overcome adversity with grace, and an experience that leaves an indelible mark on the hearts of those who venture there. It's a reminder that in a world of constant change, the timeless allure of Armenia remains a treasure waiting to be uncovered by all who seek to embrace its beauty and spirit.</p>

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
    title: "Sevanavank",
    description:
      "Perched atop the scenic Sevan Peninsula in Armenia, Sevanavank is a captivating medieval church complex. Surrounded by the glistening waters of Lake Sevan, it offers breathtaking panoramic views. The complex consists of two ancient churches, Surb Arakelots and Surb Astvatsatsin, displaying distinctive Armenian architectural elements. The tranquil ambiance, combined with the historic significance and natural beauty, makes Sevanavank a must-visit destination for cultural and visual enrichment.",
  },
  {
    src: "https://images.unsplash.com/photo-1567960095052-d15f59a1a309?ixlib=rb-4.0.3&ixid=M3wxMjA3fDB8MHxwaG90by1wYWdlfHx8fGVufDB8fHx8fA%3D%3D&auto=format&fit=crop&w=720&q=80",
    title: "Cascade",
    description:
      "The Cascade in Yerevan, Armenia, is a monumental stairway and cultural complex. Rising gracefully amidst the city's landscape, it's a fusion of modern architecture and artistic expression. The grand staircase comprises terraced levels adorned with sculptures, art installations, and lush greenery, forming an urban oasis. At the summit, the viewing platforms offer breathtaking vistas of Mount Ararat and Yerevan. The Cascade houses the Cafesjian Museum of Art, showcasing a diverse collection of contemporary and classical works. A testament to creative ingenuity, the Cascade stands as a symbol of Yerevan's vibrant cultural essence and is a popular hub for leisure, art, and admiration.",
  },
  {
    src: "https://images.unsplash.com/photo-1620982591827-5e003e8d26fb?ixlib=rb-4.0.3&ixid=M3wxMjA3fDB8MHxwaG90by1wYWdlfHx8fGVufDB8fHx8fA%3D%3D&auto=format&fit=crop&w=720&q=80",
    title: "Sevan",
    description:
      "Lake Sevan, Armenia's jewel, cradled amidst mountainous landscapes. One of the largest high-altitude lakes globally, its sapphire waters captivate all who behold. Surrounded by lush forests, the lake offers tranquility and recreation. Sevanavank Church graces its shores, a testament to history. A vital freshwater reservoir, Lake Sevan sustains biodiversity and supports local livelihoods. A haven for nature enthusiasts, seekers of solace, and those yearning for Armenian beauty.",
  },
  {
    src: "https://images.unsplash.com/photo-1598897270268-f7091c801c3d?ixlib=rb-4.0.3&ixid=M3wxMjA3fDB8MHxwaG90by1wYWdlfHx8fGVufDB8fHx8fA%3D%3D&auto=format&fit=crop&w=720&q=80",
    title: "Kentron",
    description:
      "Kentron, the heart of Yerevan, Armenia, is a vibrant urban nucleus. Lined with tree-shaded boulevards, it hosts historic landmarks, modern architecture, and cultural hotspots. Republic Square, its centerpiece, showcases grand architecture and fountains. Northern Avenue, a bustling pedestrian street, connects to Freedom Square. Cafes, shops, and galleries thrive here, intertwining past and present. The Opera House exudes elegance, while Cascade's modernity contrasts nearby classical buildings. A tapestry of cultures, Kentron resonates with Yerevan's spirit, inviting exploration and connection.",
  },
  {
    src: "https://images.unsplash.com/photo-1609931552570-9056ce113c77?ixlib=rb-4.0.3&ixid=M3wxMjA3fDB8MHxwaG90by1wYWdlfHx8fGVufDB8fHx8fA%3D%3D&auto=format&fit=crop&w=720&q=80",
    title: "Aram Khachaturian Museum",
    description:
      "The Aram Khachaturian Museum in Yerevan, Armenia, honors the renowned composer's life and work. With multimedia displays, artifacts, and interactive exhibits, it offers insight into his creative journey. Concerts and workshops further enrich the experience, making it a vibrant cultural hub celebrating Khachaturian's enduring musical legacy.",
  },
  {
    src: "https://images.unsplash.com/photo-1543060245-beb16a7e83ed?ixlib=rb-4.0.3&ixid=M3wxMjA3fDB8MHxwaG90by1wYWdlfHx8fGVufDB8fHx8fA%3D%3D&auto=format&fit=crop&w=720&q=80",
    title: "Tsitsernakaberd",
    description:
      "Tsitsernakaberd, a solemn monument in Yerevan, Armenia, stands as a poignant memorial to the Armenian Genocide. Its towering stele and twelve slabs symbolize unity and resilience. The museum underneath recounts the tragic history with artifacts and testimonials. Surrounding gardens offer solace and remembrance, inviting visitors to honor the memory of those lost and reaffirm the importance of preventing such atrocities.",
  },
];
</script>

<style scoped></style>
