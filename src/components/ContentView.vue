<template>
  <div class="content">
    <h3>This is {{ mode }} mode</h3>
    <div class="gallery-container">
      <div class="gallery-item">
        <img src="../assets/img/banner-1.jpg" alt="" />
      </div>
      <div class="gallery-item">
        <img src="../assets/img/banner-2.jpg" alt="" />
      </div>
      <div class="gallery-item">
        <img src="../assets/img/banner-3.jpg" alt="" />
      </div>
      <div class="gallery-item">
        <img src="../assets/img/banner-4.jpg" alt="" />
      </div>
      <div class="gallery-item">
        <img src="../assets/img/banner-5.jpg" alt="" />
      </div>
      <div class="gallery-item">
        <img src="../assets/img/banner-6.jpg" alt="" />
      </div>
      <div class="gallery-item">
        <img src="../assets/img/banner-7.jpg" alt="" />
      </div>
      <div class="gallery-item">
        <img src="../assets/img/banner-8.jpg" alt="" />
      </div>
      <div class="gallery-item">
        <img src="../assets/img/banner-9.jpg" alt="" />
      </div>
    </div>

    <p class="para">
      Lorem ipsum dolor sit amet consectetur adipisicing elit. Doloremque
      corrupti quod architecto neque ipsa consectetur nisi, odio, numquam optio
      dolore tenetur saepe dignissimos earum facilis adipisci animi quia
      doloribus. Dolor!
    </p>
  </div>
</template>

<script>
export default { props: ["mode"] };
</script>

<style>
.content {
  padding: 0 25px;
}
.content h3 {
  text-align: center;
  font-size: 4rem;
}

.gallery-container {
  display: flex;
  justify-content: center;
  flex-wrap: wrap;
  width: 60%;
  box-shadow: -5px -5px 15px rgba(255, 255, 255, 0.1),
    5px 5px 15px rgba(0, 0, 0, 0.35),
    inset -5px 5px 15px rgba(255, 255, 255, 0.1),
    inset 5px 5px 15px rgba(0, 0, 0, 0.35);
  margin: 0 auto;
}
.gallery-item {
  flex-basis: 32.7%;
  margin-bottom: 6px;
  opacity: 0.75;
  cursor: pointer;
  transition: 0.5s ease;
  padding: 5px;
}
.gallery-item:hover {
  opacity: 1;
  box-shadow: -5px -5px 15px rgba(255, 255, 255, 0.1),
    5px 5px 15px rgba(0, 0, 0, 0.35),
    inset -5px 5px 15px rgba(255, 255, 255, 0.1),
    inset 5px 5px 15px rgba(0, 0, 0, 0.35);
}
.gallery-item img {
  width: 100%;
  height: 100%;
  object-fit: cover;
}
.lightbox {
  display: none;
  position: fixed;
  top: 0;
  left: 0;
  width: 100%;
  height: 100%;
  background-color: rgba(0, 0, 0, 0.8);
  z-index: 9999;
}
.lightbox-content {
  position: absolute;
  top: 50%;
  left: 50%;
  transform: translate(-50%, -50%);
  text-align: center;
}
.lightbox img {
  width: 1000px;
  border-radius: 5px;
}
.lightbox-prev,
.lightbox-next {
  position: absolute;
  top: 50%;
  font-size: 30px;
  color: #fff;
  cursor: pointer;
  transform: translateY(-50%);
}
.lightbox-prev {
  left: 20px;
}
.lightbox-next {
  right: 20px;
}
.gallery-item img {
  width: 100%;
  transition: transform 0.3s ease;
}
.gallery-item:hover img {
  transform: scale(1.1);
}
.para {
  width: 100%;
  max-width: 600px;
  margin: 25px auto 0px;
}
</style>
