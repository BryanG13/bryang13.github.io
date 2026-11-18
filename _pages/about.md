---
permalink: /
title: "About me"
author_profile: true
redirect_from: 
  - /about/
  - /about.html
---

Hi, I'm ***Bryan David Galarza Montenegro***. I'm an Operations Research Expert 👨🏻‍💻 with a strong interest in designing state-of-the-art algorithms that improve decision-making in real-world systems. My career has been shaped by a fascination for complex optimisation challenges, especially those that impact transportation, logistics, and healthcare.

I am currently a **postdoctoral researcher** 🎓 at the [**ANT/OR**](https://www.uantwerpen.be/en/research-groups/ant-or/) research group at the **University of Antwerp**. Here, I work on healthcare transportation research and collaborate on the [**STRAUSS**](https://www.kuleuven.be/lim/research/projects/strauss) project, which focuses on sustainable urban logistics and the development of innovative solutions to reduce the environmental impact of city freight flows.

I have also served as the **Lead Operations Research Expert** 💼 at **Triptomatic**, contributing to a **VLAIO**-funded *development project* (an applied research project): [*AI-powered Dispatching*](https://triptomatic.com/en-be/nemt#dispatching). In this role, I led research, development and implementation on combinatorial optimisation methods to make on-demand healthcare transportation more intelligent, efficient, and scalable. At **Atlas Copco**, I also served as an improvement consultant for the packaging policy of AIRnet and piping components.

I hold a PhD 📚 in *Operations Research* from the **University of Antwerp**, where I conducted research on the design and optimisation of [*semi-flexible bus services*](https://repository.uantwerpen.be/docman/irua/5e80f4/196398.pdf). I also have a Master of Science degree in *Engineering Science: Operations Research and Industrial Engineering* from **Ghent University**.

Over the years, I have published several research papers on optimisation in intelligent transportation systems and collaborated closely with both academia and industry to bridge the gap between theory and application. 

My research interests lie in: 🚌 urban logistics, 🚑 non-emergency medical transportation, 🚍 public transportation, and 🔬 metaheuristics and exact optimisation methods.

---

🌍 Outside of work, I enjoy photography, travelling, and discovering hidden places. Exploring nature and small towns helps me recharge and often gives me new perspectives on the problems I tackle in my professional life. Browse through some photos I have taken:

<div style="text-align: center; margin: 30px 0;">
  <div style="display: inline-block; max-width: 100%;">
    <div style="display: grid; grid-template-columns: 1fr auto 1fr; align-items: center; gap: 8px; margin-bottom: 12px;">
      <button type="button" id="prevPhoto" onclick="stepPhoto(-1)" aria-label="Previous photo" onmouseover="this.style.textDecoration='underline'" onmouseout="this.style.textDecoration='none'" style="justify-self: start; cursor: pointer; background: none; border: none; padding: 0; font-size: 0.9em; color: #666;">&#8592; Previous</button>
      <span id="photoCaption" style="font-size: 0.9em; color: #666;">Loading a photo...</span>
      <button type="button" id="nextPhoto" onclick="stepPhoto(1)" aria-label="Next photo" onmouseover="this.style.textDecoration='underline'" onmouseout="this.style.textDecoration='none'" style="justify-self: end; cursor: pointer; background: none; border: none; padding: 0; font-size: 0.9em; color: #666;">Next &#8594;</button>
    </div>
    <img id="randomPhoto" src="{{ '/images/500x300.png' | relative_url }}" alt="Loading a random photograph..." style="display: block; max-width: 100%; height: auto; cursor: pointer; border-radius: 8px; box-shadow: 0 4px 6px rgba(0,0,0,0.1);" onclick="stepPhoto(1)">
  </div>
</div>

<script>
const photos = [
  { src: '/images/photos/DSC00031.JPG', caption: 'Beitou, Taiwan', trip: 'taiwan' },
  { src: '/images/photos/DSC00216.JPG', caption: 'Plane landing in Taipei Airport', trip: 'taiwan' },
  { src: '/images/photos/DSC00254.JPG', caption: 'Taipei at night', trip: 'taiwan' },
  { src: '/images/photos/DSC00364.JPG', caption: 'Views from Jiufen', trip: 'taiwan' },
  { src: '/images/photos/DSC00372.JPG', caption: 'Jiufen Old Street', trip: 'taiwan' },
  { src: '/images/photos/DSC00405.JPG', caption: 'West Coast views, Taiwan', trip: 'taiwan' },
  { src: '/images/photos/DSC00502.JPG', caption: 'Rainy days', trip: 'taiwan' },
  { src: '/images/photos/DSC00623.JPG', caption: 'Temples in Bangkok, Thailand', trip: 'thailand' },
  { src: '/images/photos/DSC00889.JPG', caption: 'Views from my stay in Bangkok', trip: 'thailand' },
  { src: '/images/photos/DSC01005.JPG', caption: 'Beach in south Thailand', trip: 'thailand' },
  { src: '/images/photos/DSC01058 (1).JPG', caption: 'Koh Phi Phi, Thailand', trip: 'thailand' },
  { src: '/images/photos/DSC01399.JPG', caption: 'Views from my stay in Kuala Lumpur', trip: 'malaysia' },
  { src: '/images/photos/DSC01555~2.JPG', caption: 'Sunset in Kota Kinabalu', trip: 'malaysia' },
  { src: '/images/photos/DSC01580.JPG', caption: 'Mosque near sunset', trip: 'malaysia' },
  { src: '/images/photos/DSC01887.JPG', caption: 'Singapore skyline', trip: 'singapore' },
  { src: '/images/photos/DSC01936.JPG', caption: 'Chinese temple in Singapore', trip: 'singapore' },
  { src: '/images/photos/DSC02041.JPG', caption: 'teamLab exhibition', trip: 'singapore' },
  { src: '/images/photos/DSC02089.JPG', caption: 'Neighbour\'s cat', trip: 'animals' },
  { src: '/images/photos/DSC02093.JPG', caption: 'Dalmatian pelicans', trip: 'animals' },
  { src: '/images/photos/DSC02216.JPG', caption: 'Lemur', trip: 'animals' },
  { src: '/images/photos/DSC02272.JPG', caption: 'Chaco chachalaca', trip: 'animals' },
  { src: '/images/photos/DSC02587.JPG', caption: 'Moorish gardens', trip: 'spain' },
  { src: '/images/photos/DSC02656.JPG', caption: 'Alcázar de Granada', trip: 'spain' },
  { src: '/images/photos/DSC02889.JPG', caption: 'Seville', trip: 'spain' },
  { src: '/images/photos/DSC03078.JPG', caption: 'Ronda landscapes', trip: 'spain' },
  { src: '/images/photos/DSC03223-01~3.jpeg', caption: 'Antwerp Station', trip: 'belgium' },
  { src: '/images/photos/DSC03282.JPG', caption: 'Spanish mountain town', trip: 'spain' },
  { src: '/images/photos/DSC03304.JPG', caption: 'Malaga', trip: 'spain' },
  { src: '/images/photos/DSC03331.JPG', caption: 'Shadows', trip: 'spain' },
  { src: '/images/photos/DSC03560.JPG', caption: 'Ronda scapes', trip: 'spain' },
  { src: '/images/photos/DSC03789-01.jpeg', caption: 'NYC at night', trip: 'usa' },
  { src: '/images/photos/DSC03833.JPG', caption: 'Chinese reflections', trip: 'china-east' },
  { src: '/images/photos/DSC04050-01.jpeg', caption: 'Peruvian vendors', trip: 'peru' },
  { src: '/images/photos/DSC04060.JPG', caption: 'Shanghai reflections', trip: 'china-east' },
  { src: '/images/photos/DSC04082-01.jpeg', caption: 'Inca ruins', trip: 'peru' },
  { src: '/images/photos/DSC04110-01.jpeg', caption: 'Salt mines', trip: 'peru' },
  { src: '/images/photos/DSC04167-01.jpeg', caption: 'Inca ruins', trip: 'peru' },
  { src: '/images/photos/DSC04168.JPG', caption: 'Snowy cat', trip: 'peru' },
  { src: '/images/photos/DSC04185-01.jpeg', caption: 'Peruvian scapes', trip: 'peru' },
  { src: '/images/photos/DSC04226.JPG', caption: 'Yellow Mountain, China', trip: 'china-east' },
  { src: '/images/photos/DSC04248.JPG', caption: 'Famous Tree', trip: 'china-east' },
  { src: '/images/photos/DSC04333-01.jpeg', caption: 'Humantay Lake', trip: 'peru' },
  { src: '/images/photos/DSC04356-01.jpeg', caption: 'Salcantay, Peru', trip: 'peru' },
  { src: '/images/photos/DSC04387-01.jpeg', caption: 'Salcantay Trek', trip: 'peru' },
  { src: '/images/photos/DSC04389.JPG', caption: 'Wangxian village', trip: 'china-chongqing' },
  { src: '/images/photos/DSC04471.JPG', caption: 'Wangxian village at night', trip: 'china-chongqing' },
  { src: '/images/photos/DSC04493-01-01.jpeg', caption: 'You know where this is ;)', trip: 'peru' },
  { src: '/images/photos/DSC04663-01.jpeg', caption: 'Alpaca Adventures', trip: 'peru' },
  { src: '/images/photos/DSC04872-01-01.jpeg', caption: 'Condor Canyon', trip: 'peru' },
  { src: '/images/photos/DSC04873-01-01.jpeg', caption: 'Condor flight', trip: 'peru' },
  { src: '/images/photos/DSC04915-01.jpeg', caption: 'Vicuñas', trip: 'peru' },
  { src: '/images/photos/DSC04916.JPG', caption: 'Water towns, China', trip: 'china-east' },
  { src: '/images/photos/DSC05007-01.jpeg', caption: 'Huacachina desert', trip: 'peru' },
  { src: '/images/photos/DSC05107-01-01.jpeg', caption: 'Lima, Peru', trip: 'peru' },
  { src: '/images/photos/DSC05120-01.jpeg', caption: 'Sunset', trip: 'peru' },
  { src: '/images/photos/DSC05168_1.JPG', caption: 'Urbanisation', trip: 'misc' },
  { src: '/images/photos/DSC05357-01.jpeg', caption: 'Cherry blossoms at sunset', trip: 'korea' },
  { src: '/images/photos/DSC05384.JPG', caption: 'A Transformers movie was filmed here', trip: 'china-chongqing' },
  { src: '/images/photos/DSC05397.JPG', caption: 'Village in Busan', trip: 'korea' },
  { src: '/images/photos/DSC05422.JPG', caption: 'Wulong', trip: 'china-chongqing' },
  { src: '/images/photos/DSC05434.JPG', caption: 'Cave waterfall', trip: 'china-chongqing' },
  { src: '/images/photos/DSC05538.JPG', caption: 'Chongqing views', trip: 'china-chongqing' },
  { src: '/images/photos/DSC05554-01.jpeg', caption: 'Spring in Korea', trip: 'korea' },
  { src: '/images/photos/DSC05600.JPG', caption: 'Bay of Chongqing', trip: 'china-chongqing' },
  { src: '/images/photos/DSC05650-01.jpeg', caption: 'Spring in Japan', trip: 'japan' },
  { src: '/images/photos/DSC05738.JPG', caption: 'Hongyadong', trip: 'china-chongqing' },
  { src: '/images/photos/DSC05815.JPG', caption: 'Forbidden City at night', trip: 'china-beijing' },
  { src: '/images/photos/DSC05849.JPG', caption: 'The Great Wall', trip: 'china-beijing' },
  { src: '/images/photos/DSC05967.JPG', caption: 'Guess where', trip: 'china-beijing' },
  { src: '/images/photos/DSC06044.JPG', caption: 'Forbidden City', trip: 'china-beijing' },
  { src: '/images/photos/DSC06069-01.jpeg', caption: 'Shinjuku', trip: 'japan' },
  { src: '/images/photos/DSC06108.JPG', caption: 'Close-up', trip: 'japan' },
  { src: '/images/photos/DSC06114.JPG', caption: 'Bee', trip: 'japan' },
  { src: '/images/photos/DSC06117.JPG', caption: 'Flowers', trip: 'japan' },
  { src: '/images/photos/DSC06128-01.jpeg', caption: 'Tokyo Tower', trip: 'japan' },
  { src: '/images/photos/DSC06142.JPG', caption: 'Duck in Bazel, Belgium', trip: 'belgium' },
  { src: '/images/photos/DSC06206~2-01.jpeg', caption: 'Famous viewpoint of Fuji-san', trip: 'japan' },
  { src: '/images/photos/DSC06245.JPG', caption: 'Fuji in spring', trip: 'japan' },
  { src: '/images/photos/DSC06322-01.jpeg', caption: 'Fuji at sundown', trip: 'japan' },
  { src: '/images/photos/DSC06409.JPG', caption: 'Reflecting ...', trip: 'japan' },
  { src: '/images/photos/DSC06494-01-01-01.jpeg', caption: 'A bit of snow', trip: 'japan' },
  { src: '/images/photos/DSC06601.JPG', caption: 'Berat', trip: 'albania' },
  { src: '/images/photos/DSC06665-01-01-01.jpeg', caption: 'Kanazawa at night', trip: 'japan' },
  { src: '/images/photos/DSC06725 (1).JPG', caption: 'Albanian beach', trip: 'albania' },
  { src: '/images/photos/DSC06819-01.jpeg', caption: 'Antwerp Cathedral', trip: 'belgium' },
  { src: '/images/photos/DSC06955.JPG', caption: 'Mirror in Atacama', trip: 'chile' },
  { src: '/images/photos/DSC06966-01-01.jpeg', caption: 'Desert sunset', trip: 'chile' },
  { src: '/images/photos/DSC06974-01.jpeg', caption: 'Atacama sunset', trip: 'chile' },
  { src: '/images/photos/DSC07026-01.jpeg', caption: 'Twin mountains', trip: 'chile' },
  { src: '/images/photos/DSC07039-01.jpeg', caption: 'Salar in Atacama', trip: 'chile' },
  { src: '/images/photos/DSC07042-01.jpeg', caption: 'Salar with views', trip: 'chile' },
  { src: '/images/photos/DSC07079-01.jpeg', caption: 'Mars, kinda', trip: 'chile' },
  { src: '/images/photos/DSC07237-01~2.jpeg', caption: 'Santiago views', trip: 'chile' },
  { src: '/images/photos/DSC07243-01~2.jpeg', caption: 'Santiago skyline', trip: 'chile' },
  { src: '/images/photos/DSC07252.JPG', caption: 'Gjirokaster Castle', trip: 'albania' },
  { src: '/images/photos/DSC07296.JPG', caption: 'Gjirokaster views', trip: 'albania' },
  { src: '/images/photos/DSC07316-01.jpeg', caption: 'The Andes from above', trip: 'ecuador' },
  { src: '/images/photos/DSC07341-01.jpeg', caption: 'Valle de los Chillos', trip: 'ecuador' },
  { src: '/images/photos/DSC07421.JPG', caption: 'Belgium from above', trip: 'belgium' },
  { src: '/images/photos/DSC07438-01.jpeg', caption: 'Lagoon in Ecuador', trip: 'ecuador' },
  { src: '/images/photos/DSC07510.JPG', caption: 'Köln sunset', trip: 'germany' },
  { src: '/images/photos/DSC07541-01.jpeg', caption: 'Wawa Pichincha', trip: 'ecuador' },
  { src: '/images/photos/DSC07682-01.jpeg', caption: 'Ecuadorian flowers', trip: 'ecuador' },
  { src: '/images/photos/DSC07688.JPG', caption: 'Koblenz views', trip: 'germany' },
  { src: '/images/photos/DSC07717.JPG', caption: 'Sunset vegetation', trip: 'germany' },
  { src: '/images/photos/DSC07725.JPG', caption: 'German sunset', trip: 'germany' },
  { src: '/images/photos/DSC07729-01.jpeg', caption: 'Cotopaxi', trip: 'ecuador' },
  { src: '/images/photos/DSC07802.JPG', caption: 'Frankfurt', trip: 'germany' },
  { src: '/images/photos/DSC07850.JPG', caption: 'Antwerp sunset', trip: 'belgium' },
  { src: '/images/photos/DSC07959-01.jpeg', caption: 'Thai temples', trip: 'thailand' },
  { src: '/images/photos/DSC08015-01.jpeg', caption: 'Bangkok from above', trip: 'thailand' },
  { src: '/images/photos/DSC08044-01-01.jpeg', caption: 'Sunset views', trip: 'thailand' },
  { src: '/images/photos/DSC08095-01.jpeg', caption: 'Humidity 100%', trip: 'thailand' },
  { src: '/images/photos/DSC08195-01.jpeg', caption: 'Tranquil sunsets', trip: 'thailand' },
  { src: '/images/photos/DSC08213-01.jpeg', caption: 'Sunset in Koh Phangan', trip: 'thailand' },
  { src: '/images/photos/DSC08308-01.jpeg', caption: 'Sandbar from above', trip: 'thailand' },
  { src: '/images/photos/DSC08313-01.jpeg', caption: 'Sandbar', trip: 'thailand' },
  { src: '/images/photos/DSC08354-01.jpeg', caption: 'Calm waters', trip: 'thailand' },
  { src: '/images/photos/DSC08478-01.jpeg', caption: 'Golden temples', trip: 'thailand' },
  { src: '/images/photos/DSC08637.JPG', caption: 'Friend', trip: 'animals' },
  { src: '/images/photos/DSC08794~2-01.jpeg', caption: 'Arab architecture', trip: 'qatar' },
  { src: '/images/photos/DSC08802-01.jpeg', caption: 'Qatar', trip: 'qatar' },
  { src: '/images/photos/DSC09183-01.jpeg', caption: 'Budapest at night', trip: 'hungary' },
  { src: '/images/photos/DSC09314-01.jpeg', caption: 'Algarve caves', trip: 'portugal' },
  { src: '/images/photos/DSC09317-01.jpeg', caption: 'Rocky beach', trip: 'portugal' },
  { src: '/images/photos/DSC09790-01.jpeg', caption: 'Alishan train', trip: 'taiwan' },
  { src: '/images/photos/DSC09990~2.JPG', caption: 'Taiwan sea of clouds', trip: 'taiwan' },
  { src: '/images/photos/IMG_0173.JPG', caption: 'Antwerp city', trip: 'belgium' },
  { src: '/images/photos/IMG_20210926_100636-01-01.jpeg', caption: 'Kotor Bay', trip: 'balkans' },
  { src: '/images/photos/IMG_20211001_122228-01.jpeg', caption: 'Game of Thrones set ;)', trip: 'balkans' },
  { src: '/images/photos/IMG_20211121_100709-01.jpeg', caption: 'Bergen hike', trip: 'norway' },
  { src: '/images/photos/PXL_20220201_084959038~2-01.jpeg', caption: 'Snowy Cappadocia', trip: 'turkey' },
  { src: '/images/photos/PXL_20220201_152844202.NIGHT-01.jpeg', caption: 'Snowy village', trip: 'turkey' },
  { src: '/images/photos/PXL_20220620_004809949-01.jpeg', caption: 'Monterrey', trip: 'mexico' },
  { src: '/images/photos/UANight.jpg', caption: 'Hof van Lieren, University of Antwerp', trip: 'belgium' },
  { src: '/images/photos/DSC00298.JPG', caption: 'Night market', trip: 'taiwan' },
  { src: '/images/photos/Chimbo.JPG', caption: 'Chimborazo, Ecuador', trip: 'ecuador' },
  { src: '/images/photos/DSC08655.JPG', caption: 'Cajas Park, Ecuador', trip: 'ecuador' },
  { src: '/images/photos/DSC07989.JPG', caption: 'Pululahua, Ecuador', trip: 'ecuador' },
  { src: '/images/photos/IMG_1548.JPG', caption: 'Nevados in Ecuador', trip: 'ecuador' },
  { src: '/images/photos/IMG_1559.JPG', caption: 'Cuicocha lake in Ecuador', trip: 'ecuador' },
  { src: '/images/photos/IMG_1565.JPG', caption: 'Imbabura volcano, Ecuador', trip: 'ecuador' },
  { src: '/images/photos/IMG_1637.JPG', caption: 'Cajas viewpoint, Ecuador', trip: 'ecuador' },
  { src: '/images/photos/IMG_1645.JPG', caption: 'Ingapirca, Ecuador', trip: 'ecuador' },
  { src: '/images/photos/IMG_1654.JPG', caption: 'Canyon near Chimborazo', trip: 'ecuador' },
  { src: '/images/photos/IMG_1849.JPG', caption: 'NY from the sky', trip: 'usa' },
  { src: '/images/photos/IMG_1856.JPG', caption: 'East coast views', trip: 'usa' },
  { src: '/images/photos/D7E5438F-A7E7-4D26-8B10-DF4E354CE45E.JPG', caption: 'Old and New', trip: 'china-south' },
  { src: '/images/photos/IMG_3302.JPG', caption: 'Calmness in Xiping', trip: 'china-south' },
  { src: '/images/photos/IMG_3333.JPG', caption: 'Views of Yangshuo', trip: 'china-south' },
  { src: '/images/photos/IMG_3335.JPG', caption: 'Ruyi Peak', trip: 'china-south' },
  { src: '/images/photos/IMG_3365.JPG', caption: 'Dong Village', trip: 'china-south' },
  { src: '/images/photos/IMG_3377.JPG', caption: 'Little village in the mountains', trip: 'china-south' },
  { src: '/images/photos/IMG_3384.JPG', caption: 'Urbanism', trip: 'china-south' },
  { src: '/images/photos/IMG_3405.JPG', caption: 'Nightlife in Guiyang', trip: 'china-south' },
  { src: '/images/photos/IMG_3415.JPG', caption: 'Guiyang scenes', trip: 'china-south' },
  { src: '/images/photos/IMG_7507.JPG', caption: 'Li Jiang Scenes', trip: 'yunnan' },
  { src: '/images/photos/IMG_7211.JPG', caption: 'Yulong Snow Mountain', trip: 'yunnan' },
  { src: '/images/photos/IMG_7260.JPG', caption: 'Shuhe', trip: 'yunnan' },
  { src: '/images/photos/IMG_7280.JPG', caption: 'Trails', trip: 'yunnan' },
  { src: '/images/photos/IMG_7304.JPG', caption: 'TGL hike', trip: 'yunnan' },
  { src: '/images/photos/IMG_7337.JPG', caption: 'Tiger Leaping Gorge', trip: 'yunnan' },
  { src: '/images/photos/IMG_7400.JPG', caption: 'Tibetan monastery', trip: 'yunnan' },
  { src: '/images/photos/IMG_7416.JPG', caption: 'Monastery', trip: 'yunnan' },
  { src: '/images/photos/IMG_7429.JPG', caption: 'Squirrel', trip: 'yunnan' },
  { src: '/images/photos/IMG_7437.JPG', caption: 'Wudi Lake', trip: 'yunnan' },
  { src: '/images/photos/IMG_7466.JPG', caption: 'Prayer flags', trip: 'yunnan' }
];

const randomPhoto = document.getElementById('randomPhoto');
const photoCaption = document.getElementById('photoCaption');
const fallbackPhoto = '{{ '/images/500x300.png' | relative_url }}';

const thumbUrl = src => src.replace('/images/photos/', '/images/photos/thumbs/').replace(/\.[^./]+$/, '.jpg');

function shuffleArray(array) {
  const shuffled = [...array];
  for (let i = shuffled.length - 1; i > 0; i--) {
    const j = Math.floor(Math.random() * (i + 1));
    [shuffled[i], shuffled[j]] = [shuffled[j], shuffled[i]];
  }
  return shuffled;
}

/* Random order, but photos from the same trip are spread evenly through the
   sequence so similar scenery rarely appears back to back. */
function spreadShuffle(items) {
  const groups = {};
  items.forEach(item => (groups[item.trip || 'misc'] ||= []).push(item));

  const placed = [];
  Object.values(groups).forEach(group => {
    const n = group.length;
    const offset = Math.random();
    shuffleArray(group).forEach((item, i) => {
      const jitter = (Math.random() - 0.5) * 0.4;
      placed.push({ item, pos: (i + offset + jitter) / n });
    });
  });
  placed.sort((a, b) => a.pos - b.pos);
  const result = placed.map(p => p.item);

  /* Fix any remaining back-to-back repeats (including the wrap-around) by
     swapping in a photo whose new neighbours are all from other trips. */
  const n = result.length;
  const trip = k => result[(k + n) % n].trip;
  const fitsAt = (k, t, skip) => [k - 1, k + 1].every(m => (m + n) % n === skip || trip(m) !== t);
  for (let i = 0; i < n; i++) {
    const a = (i + 1) % n;
    if (trip(i) !== trip(a)) continue;
    for (let b = 0; b < n; b++) {
      if (b === a || trip(b) === trip(a)) continue;
      if (fitsAt(a, trip(b), b) && fitsAt(b, trip(a), a)) {
        [result[a], result[b]] = [result[b], result[a]];
        break;
      }
    }
  }
  return result;
}

const shuffledPhotos = spreadShuffle(photos);
let currentPhotoIndex = shuffledPhotos.length ? Math.floor(Math.random() * shuffledPhotos.length) : 0;
let currentSrc = '';

function showPhoto() {
  const photo = shuffledPhotos[currentPhotoIndex];
  const src = thumbUrl(photo.src);

  if (src === currentSrc) return;
  currentSrc = src;

  randomPhoto.onerror = () => {
    randomPhoto.onerror = null;
    randomPhoto.alt = 'Photo unavailable';
    randomPhoto.src = fallbackPhoto;
    photoCaption.textContent = 'Photo unavailable';
  };
  randomPhoto.alt = photo.caption || 'Photograph';
  randomPhoto.src = src;
  photoCaption.textContent = photo.caption || '';

  const next = shuffledPhotos[(currentPhotoIndex + 1) % shuffledPhotos.length];
  if (next) new Image().src = thumbUrl(next.src);
}

function stepPhoto(direction) {
  if (!shuffledPhotos.length) return;
  currentPhotoIndex = (currentPhotoIndex + direction + shuffledPhotos.length) % shuffledPhotos.length;
  showPhoto();
}

function initPhotoGallery() {
  if (!randomPhoto || !photoCaption) return;
  showPhoto();
}

if (document.readyState === 'loading') {
  window.addEventListener('DOMContentLoaded', initPhotoGallery, { once: true });
} else {
  initPhotoGallery();
}
</script>  