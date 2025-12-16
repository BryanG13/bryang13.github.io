---
permalink: /
title: "About me"
author_profile: true
redirect_from: 
  - /about/
  - /about.html
---

Hi, I'm ***Bryan David Galarza Montenegro***. I'm an Operations Research Expert with a strong interest in designing state-of-the-art algorithms that improve decision-making in real-world systems. My career has been shaped by a fascination for complex optimization challenges, especially those that impact transportation, logistics, and healthcare.

I am currently a **postdoctoral researcher** 🎓 at the [**ANT/OR**](https://www.uantwerpen.be/en/research-groups/ant-or/) research group in the **University of Antwerp**. Here, I work on healthcare transportation research on and the [**STRAUSS**](https://www.kuleuven.be/lim/research/projects/strauss) project, which focuses on sustainable urban logistics and the development of innovative solutions to reduce the environmental impact of city freight flows.

I have also served as the **Lead Operations Research Expert** at **Triptomatic**, contributing to a **VLAIO**-funded *development project*: [*AI-powered Dispatching*](https://triptomatic.com/en-be/nemt#dispatching). In this role, I lead research, development and implementation on combinatorial optimization methods to make on-demand healthcare transportation more intelligent, efficient, and scalable. In **Atlas Copco**, I also served as an improvement consultant for the packaging policy of compressor parts.

I hold a PhD 📚  in *Operations Research* from the **University of Antwerp**, where I conducted research on the design and optimization of [*semi-flexible bus services*](https://repository.uantwerpen.be/docman/irua/5e80f4/196398.pdf). I also have Master of Science degree in *Engineering Science: Operations Research and Industrial Engineering* from **Ghent University**.

Over the years, I have published several research papers on optimization in intelligent transportation systems and collaborated closely with both academia and industry to bridge the gap between theory and application. My research interests lie in: 🚌 urban logistics, 🚑 non-emergency medical transportation, 🚍 public transportation, and 🔬 metaheuristics and exact optimization methods

---

🌍 Outside of work, I enjoy photography, traveling, and discovering hidden places. Exploring nature and small towns helps me recharge and often gives me new perspectives on the problems I tackle in my professional life. Here below, you can click to view a random photo I have taken!

<div style="text-align: center; margin: 30px 0;">
  <img id="randomPhoto" src="" alt="Random photo" style="max-width: 100%; height: auto; cursor: pointer; border-radius: 8px; box-shadow: 0 4px 6px rgba(0,0,0,0.1);" onclick="changePhoto()">
  <p style="font-size: 0.9em; color: #666; margin-top: 10px;">Click the photo to see another one!</p>
</div>

<script>
const photos = [
  '/images/photos/DSC00254.JPG',
  '/images/photos/DSC00372.JPG',
  '/images/photos/DSC00405.JPG',
  '/images/photos/DSC00502.JPG',
  '/images/photos/DSC01058 (1).JPG',
  '/images/photos/DSC01399.JPG',
  '/images/photos/DSC02216.JPG',
  '/images/photos/DSC02272.JPG',
  '/images/photos/DSC02583.JPG',
  '/images/photos/DSC02655.JPG',
  '/images/photos/DSC03088.JPG',
  '/images/photos/DSC03223-01~3.jpeg',
  '/images/photos/DSC03282.JPG',
  '/images/photos/DSC03302.JPG',
  '/images/photos/DSC03331.JPG',
  '/images/photos/DSC04060.JPG',
  '/images/photos/DSC04082-01.jpeg',
  '/images/photos/DSC04110-01.jpeg',
  '/images/photos/DSC04168.JPG',
  '/images/photos/DSC04185-01.jpeg',
  '/images/photos/DSC04248.JPG',
  '/images/photos/DSC04267-01.jpeg',
  '/images/photos/DSC04333-01.jpeg',
  '/images/photos/DSC04356-01.jpeg',
  '/images/photos/DSC04387-01.jpeg',
  '/images/photos/DSC04471.JPG',
  '/images/photos/DSC04493-01-01.jpeg',
  '/images/photos/DSC04663-01.jpeg',
  '/images/photos/DSC04873-01-01.jpeg',
  '/images/photos/DSC04915-01.jpeg',
  '/images/photos/DSC04916.JPG',
  '/images/photos/DSC05007-01.jpeg',
  '/images/photos/DSC05357-01.jpeg',
  '/images/photos/DSC05600.JPG',
  '/images/photos/DSC05650-01.jpeg',
  '/images/photos/DSC05733.JPG',
  '/images/photos/DSC05965.JPG',
  '/images/photos/DSC06044.JPG',
  '/images/photos/DSC06069-01.jpeg',
  '/images/photos/DSC06128-01.jpeg',
  '/images/photos/DSC06245.JPG',
  '/images/photos/DSC06322-01.jpeg',
  '/images/photos/DSC06494-01-01-01.jpeg',
  '/images/photos/DSC06603.JPG',
  '/images/photos/DSC06819-01.jpeg',
  '/images/photos/DSC06955.JPG',
  '/images/photos/DSC07026-01.jpeg',
  '/images/photos/DSC07039-01.jpeg',
  '/images/photos/DSC07042-01.jpeg',
  '/images/photos/DSC07079-01.jpeg',
  '/images/photos/DSC07252.JPG',
  '/images/photos/DSC07316-01.jpeg',
  '/images/photos/DSC07421.JPG',
  '/images/photos/DSC07438-01.jpeg',
  '/images/photos/DSC07541-01.jpeg',
  '/images/photos/DSC07717.JPG',
  '/images/photos/DSC07725.JPG',
  '/images/photos/DSC07729-01.jpeg',
  '/images/photos/DSC07970-01.jpeg',
  '/images/photos/DSC08015-01.jpeg',
  '/images/photos/DSC08044-01-01.jpeg',
  '/images/photos/DSC08195-01.jpeg',
  '/images/photos/DSC08308-01.jpeg',
  '/images/photos/DSC08313-01.jpeg',
  '/images/photos/DSC08354-01.jpeg',
  '/images/photos/DSC08794~2-01.jpeg',
  '/images/photos/DSC09183-01.jpeg',
  '/images/photos/DSC09314-01.jpeg',
  '/images/photos/DSC09317-01.jpeg',
  '/images/photos/DSC09790-01.jpeg',
  '/images/photos/DSC09990~2.JPG'
];

let currentPhotoIndex = -1;

function changePhoto() {
  let newIndex;
  do {
    newIndex = Math.floor(Math.random() * photos.length);
  } while (newIndex === currentPhotoIndex && photos.length > 1);
  
  currentPhotoIndex = newIndex;
  document.getElementById('randomPhoto').src = photos[currentPhotoIndex];
}

// Load initial random photo when page loads
window.addEventListener('DOMContentLoaded', changePhoto);
</script>  

