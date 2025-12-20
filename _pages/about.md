---
permalink: /
title: "About me"
author_profile: true
redirect_from: 
  - /about/
  - /about.html
---

Hi, I'm ***Bryan David Galarza Montenegro***. I'm an Operations Research Expert 👨🏻‍💻 with a strong interest in designing state-of-the-art algorithms that improve decision-making in real-world systems. My career has been shaped by a fascination for complex optimization challenges, especially those that impact transportation, logistics, and healthcare.

I am currently a **postdoctoral researcher** 🎓 at the [**ANT/OR**](https://www.uantwerpen.be/en/research-groups/ant-or/) research group in the **University of Antwerp**. Here, I work on healthcare transportation research on and the [**STRAUSS**](https://www.kuleuven.be/lim/research/projects/strauss) project, which focuses on sustainable urban logistics and the development of innovative solutions to reduce the environmental impact of city freight flows.

I have also served as the **Lead Operations Research Expert** 💼 at **Triptomatic**, contributing to a **VLAIO**-funded *development project*: [*AI-powered Dispatching*](https://triptomatic.com/en-be/nemt#dispatching). In this role, I lead research, development and implementation on combinatorial optimization methods to make on-demand healthcare transportation more intelligent, efficient, and scalable. In **Atlas Copco**, I also served as an improvement consultant for the packaging policy of compressor parts.

I hold a PhD 📚 in *Operations Research* from the **University of Antwerp**, where I conducted research on the design and optimization of [*semi-flexible bus services*](https://repository.uantwerpen.be/docman/irua/5e80f4/196398.pdf). I also have Master of Science degree in *Engineering Science: Operations Research and Industrial Engineering* from **Ghent University**.

Over the years, I have published several research papers on optimization in intelligent transportation systems and collaborated closely with both academia and industry to bridge the gap between theory and application. 

My research interests lie in: 🚌 urban logistics, 🚑 non-emergency medical transportation, 🚍 public transportation, and 🔬 metaheuristics and exact optimization methods

---

🌍 Outside of work, I enjoy photography, traveling, and discovering hidden places. Exploring nature and small towns helps me recharge and often gives me new perspectives on the problems I tackle in my professional life. Here below, you can click to view a random photo I have taken! 

Keep clicking on a picture to view more:
<div style="text-align: center; margin: 30px 0;">
  <img id="randomPhoto" src="" alt="Click to start viewing my photography!" style="max-width: 100%; height: auto; cursor: pointer; border-radius: 8px; box-shadow: 0 4px 6px rgba(0,0,0,0.1);" onclick="changePhoto()">
  <p id="photoCaption" style="font-size: 0.9em; color: #666; margin-top: 10px;">Click the photo to see another one!</p>
</div>

<script>
const photos = [
  { src: '/images/photos/DSC00031.JPG', caption: 'Beitou, Taiwan' },
  { src: '/images/photos/DSC00216.JPG', caption: 'Plane landing in Taipei Airport' },
  { src: '/images/photos/DSC00254.JPG', caption: 'Taipei at night' },
  { src: '/images/photos/DSC00364.JPG', caption: 'Views from Jiufen' },
  { src: '/images/photos/DSC00372.JPG', caption: 'Jiufen Old Street' },
  { src: '/images/photos/DSC00405.JPG', caption: 'West Coast views, Taiwan' },
  { src: '/images/photos/DSC00502.JPG', caption: 'Rainy days' },
  { src: '/images/photos/DSC00623.JPG', caption: 'Temples in Bangkok, Thailand' },
  { src: '/images/photos/DSC00889.JPG', caption: 'Views from my stay in Bangkok' },
  { src: '/images/photos/DSC01005.JPG', caption: 'Beach in south Thailand' },
  { src: '/images/photos/DSC01058 (1).JPG', caption: 'Koh Phi Phi, Thailand' },
  { src: '/images/photos/DSC01399.JPG', caption: 'Views from my stay in Kuala Lumpur' },
  { src: '/images/photos/DSC01555~2.JPG', caption: 'Sunset in Kota Kinabalu' },
  { src: '/images/photos/DSC01580.JPG', caption: 'Mosque near sunset' },
  { src: '/images/photos/DSC01887.JPG', caption: 'Singapore skyline' },
  { src: '/images/photos/DSC01936.JPG', caption: 'Chinese temple in Singapore' },
  { src: '/images/photos/DSC02041.JPG', caption: 'TeamLabs exhibition' },
  { src: '/images/photos/DSC02089.JPG', caption: 'Neighbour\'s cat' },
  { src: '/images/photos/DSC02093.JPG', caption: 'Dalmatian pelicans' },
  { src: '/images/photos/DSC02216.JPG', caption: 'Lemur' },
  { src: '/images/photos/DSC02272.JPG', caption: 'Chaco chachalaca' },
  { src: '/images/photos/DSC02587.JPG', caption: 'Moorish gardens' },
  { src: '/images/photos/DSC02656.JPG', caption: 'Alcázar de Granada' },
  { src: '/images/photos/DSC02889.JPG', caption: 'Seville' },
  { src: '/images/photos/DSC03078.JPG', caption: 'Ronda landscapes' },
  { src: '/images/photos/DSC03223-01~3.jpeg', caption: 'Antwerp Station' },
  { src: '/images/photos/DSC03282.JPG', caption: 'Spanish mountain town' },
  { src: '/images/photos/DSC03304.JPG', caption: 'Malaga' },
  { src: '/images/photos/DSC03331.JPG', caption: 'Shadows' },
  { src: '/images/photos/DSC03560.JPG', caption: 'Ronda scapes' },
  { src: '/images/photos/DSC03789-01.jpeg', caption: 'NYC at night' },
  { src: '/images/photos/DSC03833.JPG', caption: 'Chinese reflections' },
  { src: '/images/photos/DSC04050-01.jpeg', caption: 'Peruvian vendors' },
  { src: '/images/photos/DSC04060.JPG', caption: 'Shanghai reflections' },
  { src: '/images/photos/DSC04082-01.jpeg', caption: 'Inca ruins' },
  { src: '/images/photos/DSC04110-01.jpeg', caption: 'Salt mines' },
  { src: '/images/photos/DSC04167-01.jpeg', caption: 'Inca ruins' },
  { src: '/images/photos/DSC04168.JPG', caption: 'Snowy cat' },
  { src: '/images/photos/DSC04185-01.jpeg', caption: 'Peruvian scapes' },
  { src: '/images/photos/DSC04226.JPG', caption: 'Yellow Mountain, China' },
  { src: '/images/photos/DSC04248.JPG', caption: 'Famous Tree' },
  { src: '/images/photos/DSC04267-01.jpeg', caption: 'Cusco viewpoint' },
  { src: '/images/photos/DSC04281-01.jpeg', caption: 'Cusco, Peru' },
  { src: '/images/photos/DSC04333-01.jpeg', caption: 'Humantay Lake' },
  { src: '/images/photos/DSC04356-01.jpeg', caption: 'Salcantay, Peru' },
  { src: '/images/photos/DSC04387-01.jpeg', caption: 'Salcantay Trek' },
  { src: '/images/photos/DSC04389.JPG', caption: 'Wangxian village' },
  { src: '/images/photos/DSC04471.JPG', caption: 'Wangxian village at night' },
  { src: '/images/photos/DSC04493-01-01.jpeg', caption: 'You know where this is ;)' },
  { src: '/images/photos/DSC04663-01.jpeg', caption: 'Alpaca Adventures' },
  { src: '/images/photos/DSC04696-01.jpeg', caption: 'Rainbow mountains' },
  { src: '/images/photos/DSC04872-01-01.jpeg', caption: 'Condor Canyon' },
  { src: '/images/photos/DSC04873-01-01.jpeg', caption: 'Condor flight' },
  { src: '/images/photos/DSC04915-01.jpeg', caption: 'Vicuñas' },
  { src: '/images/photos/DSC04916.JPG', caption: 'Water towns, China' },
  { src: '/images/photos/DSC05007-01.jpeg', caption: 'Huacachina desert' },
  { src: '/images/photos/DSC05107-01-01.jpeg', caption: 'Lima, Peru' },
  { src: '/images/photos/DSC05120-01.jpeg', caption: 'Sunset' },
  { src: '/images/photos/DSC05168_1.JPG', caption: 'Urbanisation' },
  { src: '/images/photos/DSC05357-01.jpeg', caption: 'Cherry blossoms at sunset' },
  { src: '/images/photos/DSC05384.JPG', caption: 'A transformers movie was filmed here' },
  { src: '/images/photos/DSC05397.JPG', caption: 'Village in Busan' },
  { src: '/images/photos/DSC05422.JPG', caption: 'Wulong' },
  { src: '/images/photos/DSC05434.JPG', caption: 'Cave waterfall' },
  { src: '/images/photos/DSC05538.JPG', caption: 'Chongqing views' },
  { src: '/images/photos/DSC05554-01.jpeg', caption: 'Spring in Korea' },
  { src: '/images/photos/DSC05600.JPG', caption: 'Bay of Chongqing' },
  { src: '/images/photos/DSC05650-01.jpeg', caption: 'Spring in Japan' },
  { src: '/images/photos/DSC05738.JPG', caption: 'Hongyadong' },
  { src: '/images/photos/DSC05815.JPG', caption: 'Forbidden city at night' },
  { src: '/images/photos/DSC05849.JPG', caption: 'The great wall' },
  { src: '/images/photos/DSC05967.JPG', caption: 'Guess where' },
  { src: '/images/photos/DSC06044.JPG', caption: 'Forbidden city' },
  { src: '/images/photos/DSC06069-01.jpeg', caption: 'Shinjuku' },
  { src: '/images/photos/DSC06108.JPG', caption: 'Close-up' },
  { src: '/images/photos/DSC06114.JPG', caption: 'Bee' },
  { src: '/images/photos/DSC06117.JPG', caption: 'Flowers' },
  { src: '/images/photos/DSC06128-01.jpeg', caption: 'Tokyo tower' },
  { src: '/images/photos/DSC06142.JPG', caption: 'Duck in Bazel, Belgium' },
  { src: '/images/photos/DSC06206~2-01.jpeg', caption: 'Famous view point of Fuji-san' },
  { src: '/images/photos/DSC06245.JPG', caption: 'Fuji in spring' },
  { src: '/images/photos/DSC06322-01.jpeg', caption: 'Fuji at sundown' },
  { src: '/images/photos/DSC06409.JPG', caption: 'Reflecting ...' },
  { src: '/images/photos/DSC06494-01-01-01.jpeg', caption: 'A bit of snow' },
  { src: '/images/photos/DSC06601.JPG', caption: 'Berat' },
  { src: '/images/photos/DSC06665-01-01-01.jpeg', caption: 'Kanazawa at night' },
  { src: '/images/photos/DSC06725 (1).JPG', caption: 'Albanian beach' },
  { src: '/images/photos/DSC06819-01.jpeg', caption: 'Antwerp Cathedral' },
  { src: '/images/photos/DSC06955.JPG', caption: 'Mirror in Atacama' },
  { src: '/images/photos/DSC06966-01-01.jpeg', caption: 'Desert sunset' },
  { src: '/images/photos/DSC06974-01.jpeg', caption: 'Atacama sunset' },
  { src: '/images/photos/DSC07026-01.jpeg', caption: 'Twin mountains' },
  { src: '/images/photos/DSC07039-01.jpeg', caption: 'Salar in Atacama' },
  { src: '/images/photos/DSC07042-01.jpeg', caption: 'Salar with views' },
  { src: '/images/photos/DSC07079-01.jpeg', caption: 'Mars, kinda' },
  { src: '/images/photos/DSC07237-01~2.jpeg', caption: 'Santiago views' },
  { src: '/images/photos/DSC07243-01~2.jpeg', caption: 'Santiago skyline' },
  { src: '/images/photos/DSC07252.JPG', caption: 'Gjirokaster Castle' },
  { src: '/images/photos/DSC07296.JPG', caption: 'Gjirokaster views' },
  { src: '/images/photos/DSC07316-01.jpeg', caption: 'The Andes from above' },
  { src: '/images/photos/DSC07341-01.jpeg', caption: 'Valle de los Chillos' },
  { src: '/images/photos/DSC07421.JPG', caption: 'Belgium from above' },
  { src: '/images/photos/DSC07438-01.jpeg', caption: 'Lagoon in Ecuador' },
  { src: '/images/photos/DSC07510.JPG', caption: 'Koln sunset' },
  { src: '/images/photos/DSC07541-01.jpeg', caption: 'Wawa Pichincha' },
  { src: '/images/photos/DSC07682-01.jpeg', caption: 'Ecuadorian flowers' },
  { src: '/images/photos/DSC07688.JPG', caption: 'Koblenz views' },
  { src: '/images/photos/DSC07717.JPG', caption: 'Sunset vegetation' },
  { src: '/images/photos/DSC07725.JPG', caption: 'German sunset' },
  { src: '/images/photos/DSC07729-01.jpeg', caption: 'Cotopaxi' },
  { src: '/images/photos/DSC07802.JPG', caption: 'Frankfurt' },
  { src: '/images/photos/DSC07850.JPG', caption: 'Antwerp sunset' },
  { src: '/images/photos/DSC07959-01.jpeg', caption: 'Thai temples' },
  { src: '/images/photos/DSC08015-01.jpeg', caption: 'Bangkok from above' },
  { src: '/images/photos/DSC08044-01-01.jpeg', caption: 'Sunset views' },
  { src: '/images/photos/DSC08095-01.jpeg', caption: 'Humidity 100%' },
  { src: '/images/photos/DSC08195-01.jpeg', caption: 'Tranquil sunsets' },
  { src: '/images/photos/DSC08213-01.jpeg', caption: 'Sunset in Koh Phangan' },
  { src: '/images/photos/DSC08308-01.jpeg', caption: 'Sand bar from above' },
  { src: '/images/photos/DSC08313-01.jpeg', caption: 'Sand bar' },
  { src: '/images/photos/DSC08354-01.jpeg', caption: 'Calm waters' },
  { src: '/images/photos/DSC08478-01.jpeg', caption: 'Golden temples' },
  { src: '/images/photos/DSC08637.JPG', caption: 'Friend' },
  { src: '/images/photos/DSC08794~2-01.jpeg', caption: 'Arab architecture' },
  { src: '/images/photos/DSC08802-01.jpeg', caption: 'Qatar' },
  { src: '/images/photos/DSC09183-01.jpeg', caption: 'Budapest at night' },
  { src: '/images/photos/DSC09314-01.jpeg', caption: 'Algarve caves' },
  { src: '/images/photos/DSC09317-01.jpeg', caption: 'Rocky beach' },
  { src: '/images/photos/DSC09790-01.jpeg', caption: 'Alishan train' },
  { src: '/images/photos/DSC09990~2.JPG', caption: 'Taiwan sea of clouds' },
  { src: '/images/photos/IMG_0173.JPG', caption: 'Antwerp city' },
  { src: '/images/photos/IMG_20210926_100636-01-01.jpeg', caption: 'Kotor Bay' },
  { src: '/images/photos/IMG_20211001_122228-01.jpeg', caption: 'Game of Thrones set ;)' },
  { src: '/images/photos/IMG_20211121_100709-01.jpeg', caption: 'Bergen hike' },
  { src: '/images/photos/PXL_20220201_084959038~2-01.jpeg', caption: 'Snowy Cappadocia' },
  { src: '/images/photos/PXL_20220201_152844202.NIGHT-01.jpeg', caption: 'Snowy village' },
  { src: '/images/photos/PXL_20220620_004809949-01.jpeg', caption: 'Monterrey' },
  { src: '/images/photos/UANight.jpg', caption: 'Hof van Lieren, University of Antwerp' }
];

let shuffledPhotos = [];
let currentPhotoIndex = 0;
let isShuffled = false;

function shuffleArray(array) {
  const shuffled = [...array];
  for (let i = shuffled.length - 1; i > 0; i--) {
    const j = Math.floor(Math.random() * (i + 1));
    [shuffled[i], shuffled[j]] = [shuffled[j], shuffled[i]];
  }
  return shuffled;
}

function changePhoto() {
  if (!isShuffled) {
    shuffledPhotos = shuffleArray(photos);
    isShuffled = true;
  }
  
  const currentPhoto = shuffledPhotos[currentPhotoIndex];
  document.getElementById('randomPhoto').src = currentPhoto.src;
  
  const captionElement = document.getElementById('photoCaption');
  if (currentPhoto.caption) {
    captionElement.textContent = currentPhoto.caption;
  } else {
    captionElement.textContent = 'Click the photo to see another one!';
  }
  
  currentPhotoIndex = (currentPhotoIndex + 1) % shuffledPhotos.length;
}

// Load initial random photo when page loads
window.addEventListener('DOMContentLoaded', changePhoto);
</script>  