<script>
  import {fade,fly} from 'svelte-transitions'
</script>

<style lang="scss">
  .Tattos {
    margin-top: 13vh;
    width: 80vw;
    margin: 20px auto;
    columns: 3;
    column-gap: 40px;
    .box {
      max-width: 100%;
      margin: 0 0 0 20px;
      padding: 10px;
      overflow: hidden;
      break-inside: avoid;
      img {
        width: 100%;
        border-radius: 20px;
        transition: 1s;
      }
      img:hover {
        filter: grayscale(100%);
        transform: scale(1.1);
      }
    }
  }
  @media (max-width: 1200px) {
    .Tattos {
      columns: 2;
    }
  }
  @media (max-width: 657px) {
    .Tattos {
      columns: 1;
    }
  }
</style>

<div class="Tattos" in:fade  out:fly="{{ y: 200, duration: 1500 }}">
  <div class="box">
    <a
      href="https://instagram.faqp4-1.fna.fbcdn.net/v/t51.2885-15/sh0.08/e35/p640x640/118472261_121828239388533_1708653920161727012_n.jpg?_nc_ht=instagram.faqp4-1.fna.fbcdn.net&_nc_cat=109&_nc_ohc=-vESmVftkQ8AX9PmsZ1&oh=d22835e89e8c358c9512ecb70087646b&oe=5F8DCC31"><img
        src="https://instagram.faqp4-1.fna.fbcdn.net/v/t51.2885-15/sh0.08/e35/p640x640/118472261_121828239388533_1708653920161727012_n.jpg?_nc_ht=instagram.faqp4-1.fna.fbcdn.net&_nc_cat=109&_nc_ohc=-vESmVftkQ8AX9PmsZ1&oh=d22835e89e8c358c9512ecb70087646b&oe=5F8DCC31"
        alt="images.jpg" /></a>
  </div>
  <div class="box">
    <a
      href="https://instagram.faqp4-1.fna.fbcdn.net/v/t51.2885-15/sh0.08/e35/s750x750/118502864_599623174257302_1926625793393637919_n.jpg?_nc_ht=instagram.faqp4-1.fna.fbcdn.net&_nc_cat=102&_nc_ohc=GThztPIRnYcAX97JwZr&oh=c0d10e56f7e96bcd358bf083c4a653a7&oe=5F8CCA4B"><img
        src="https://instagram.faqp4-1.fna.fbcdn.net/v/t51.2885-15/sh0.08/e35/s750x750/118502864_599623174257302_1926625793393637919_n.jpg?_nc_ht=instagram.faqp4-1.fna.fbcdn.net&_nc_cat=102&_nc_ohc=GThztPIRnYcAX97JwZr&oh=c0d10e56f7e96bcd358bf083c4a653a7&oe=5F8CCA4B"
        alt="" /></a>
  </div>
  <div class="box">
    <a
      href="https://instagram.faqp4-1.fna.fbcdn.net/v/t51.2885-15/e35/118255315_618406118816091_3842686074142679728_n.jpg?_nc_ht=instagram.faqp4-1.fna.fbcdn.net&_nc_cat=103&_nc_ohc=0iR25YMqm2MAX9F-lF6&_nc_tp=18&oh=43273017c772330cf8c223f20decf87c&oe=5F8BBE9F"><img
        src="https://instagram.faqp4-1.fna.fbcdn.net/v/t51.2885-15/e35/118255315_618406118816091_3842686074142679728_n.jpg?_nc_ht=instagram.faqp4-1.fna.fbcdn.net&_nc_cat=103&_nc_ohc=0iR25YMqm2MAX9F-lF6&_nc_tp=18&oh=43273017c772330cf8c223f20decf87c&oe=5F8BBE9F"
        alt="" /></a>
  </div>
  <div class="box">
    <a
      href="https://instagram.faqp4-1.fna.fbcdn.net/v/t51.2885-15/e35/105299945_603194843502155_5414964199801122074_n.jpg?_nc_ht=instagram.faqp4-1.fna.fbcdn.net&_nc_cat=111&_nc_ohc=__ddTQqpphAAX9mjMZE&_nc_tp=18&oh=a19c2e426011bb615ef36dcdd8b32561&oe=5F8C5DFE"><img
        src="https://instagram.faqp4-1.fna.fbcdn.net/v/t51.2885-15/e35/105299945_603194843502155_5414964199801122074_n.jpg?_nc_ht=instagram.faqp4-1.fna.fbcdn.net&_nc_cat=111&_nc_ohc=__ddTQqpphAAX9mjMZE&_nc_tp=18&oh=a19c2e426011bb615ef36dcdd8b32561&oe=5F8C5DFE"
        alt="" /></a>
  </div>
  <div class="box">
    <a
      href="https://instagram.faqp4-2.fna.fbcdn.net/v/t51.2885-15/sh0.08/e35/s640x640/105936585_164158198501876_6534170078573408679_n.jpg?_nc_ht=instagram.faqp4-2.fna.fbcdn.net&_nc_cat=104&_nc_ohc=EqhT6PXe5aEAX_rwbBr&oh=2d3cc63766ffec1b578db75a06ba2762&oe=5F8A4F9B"><img
        src="https://instagram.faqp4-2.fna.fbcdn.net/v/t51.2885-15/sh0.08/e35/s640x640/105936585_164158198501876_6534170078573408679_n.jpg?_nc_ht=instagram.faqp4-2.fna.fbcdn.net&_nc_cat=104&_nc_ohc=EqhT6PXe5aEAX_rwbBr&oh=2d3cc63766ffec1b578db75a06ba2762&oe=5F8A4F9B"
        alt="images.jpg" /></a>
  </div>
  <div class="box">
    <a
      href="https://instagram.faqp4-2.fna.fbcdn.net/v/t51.2885-15/sh0.08/e35/p750x750/93989092_1099326240423652_2612036512722179655_n.jpg?_nc_ht=instagram.faqp4-2.fna.fbcdn.net&_nc_cat=104&_nc_ohc=RZme8WgDQYgAX8Ry7Lu&oh=6e5a45870f0b8deb048d2f54befea540&oe=5F8D6A1E"><img
        src="https://instagram.faqp4-2.fna.fbcdn.net/v/t51.2885-15/sh0.08/e35/p750x750/93989092_1099326240423652_2612036512722179655_n.jpg?_nc_ht=instagram.faqp4-2.fna.fbcdn.net&_nc_cat=104&_nc_ohc=RZme8WgDQYgAX8Ry7Lu&oh=6e5a45870f0b8deb048d2f54befea540&oe=5F8D6A1E"
        alt="images.jpg" /></a>
  </div>
  <div class="box">
    <a
      href="https://instagram.faqp4-2.fna.fbcdn.net/v/t51.2885-15/sh0.08/e35/s750x750/79515082_232722021049375_9148320603167712913_n.jpg?_nc_ht=instagram.faqp4-2.fna.fbcdn.net&_nc_cat=107&_nc_ohc=DcdZTrfQs7kAX-yxH2a&oh=307457df4190b6816ad747c664958514&oe=5F8DDEA3"><img
        src="https://instagram.faqp4-2.fna.fbcdn.net/v/t51.2885-15/sh0.08/e35/s750x750/79515082_232722021049375_9148320603167712913_n.jpg?_nc_ht=instagram.faqp4-2.fna.fbcdn.net&_nc_cat=107&_nc_ohc=DcdZTrfQs7kAX-yxH2a&oh=307457df4190b6816ad747c664958514&oe=5F8DDEA3"
        alt="images.jpg" /></a>
  </div>
  <div class="box">
    <a
      href="https://instagram.faqp4-2.fna.fbcdn.net/v/t51.2885-15/sh0.08/e35/p750x750/75483250_2374248522879388_2163315578318288423_n.jpg?_nc_ht=instagram.faqp4-2.fna.fbcdn.net&_nc_cat=104&_nc_ohc=oLHuOBC1vAkAX_4B0zx&oh=bf7a495d622c447fd6f060a3f68b8eca&oe=5F8D0038"><img
        src="https://instagram.faqp4-2.fna.fbcdn.net/v/t51.2885-15/sh0.08/e35/p750x750/75483250_2374248522879388_2163315578318288423_n.jpg?_nc_ht=instagram.faqp4-2.fna.fbcdn.net&_nc_cat=104&_nc_ohc=oLHuOBC1vAkAX_4B0zx&oh=bf7a495d622c447fd6f060a3f68b8eca&oe=5F8D0038"
        alt="images.jpg" /></a>
  </div>
  <div class="box">
    <a
      href="https://instagram.faqp4-2.fna.fbcdn.net/v/t51.2885-15/sh0.08/e35/p750x750/59320278_2008912229418713_5922267333472594941_n.jpg?_nc_ht=instagram.faqp4-2.fna.fbcdn.net&_nc_cat=105&_nc_ohc=GdiJiwulVNAAX-_9nsA&oh=79bbbd5aa2aeef9fe66e935f9f6e45aa&oe=5F8A2DE6"><img
        src="https://instagram.faqp4-2.fna.fbcdn.net/v/t51.2885-15/sh0.08/e35/p750x750/59320278_2008912229418713_5922267333472594941_n.jpg?_nc_ht=instagram.faqp4-2.fna.fbcdn.net&_nc_cat=105&_nc_ohc=GdiJiwulVNAAX-_9nsA&oh=79bbbd5aa2aeef9fe66e935f9f6e45aa&oe=5F8A2DE6"
        alt="images.jpg" /></a>
  </div>
  <div class="box">
    <a
      href="https://scontent.faqp4-1.fna.fbcdn.net/v/t1.0-9/118952195_600961800586662_6905456992726952178_o.jpg?_nc_cat=103&_nc_sid=a26aad&_nc_eui2=AeEF0hsBqrPZ3Ab8FML-9QsCi7XDAYCft3WLtcMBgJ-3daXe5xpsOjkZd_yKbXC5xVd0MdwtsO1YKZcBgf0LEFNQ&_nc_ohc=_hQWR3fG85MAX91dtyf&_nc_ht=scontent.faqp4-1.fna&oh=2d45dadefec30ba4598c765388d2e415&oe=5F897D6A"><img
        src="https://scontent.faqp4-1.fna.fbcdn.net/v/t1.0-9/118952195_600961800586662_6905456992726952178_o.jpg?_nc_cat=103&_nc_sid=a26aad&_nc_eui2=AeEF0hsBqrPZ3Ab8FML-9QsCi7XDAYCft3WLtcMBgJ-3daXe5xpsOjkZd_yKbXC5xVd0MdwtsO1YKZcBgf0LEFNQ&_nc_ohc=_hQWR3fG85MAX91dtyf&_nc_ht=scontent.faqp4-1.fna&oh=2d45dadefec30ba4598c765388d2e415&oe=5F897D6A"
        alt="images.jpg" /></a>
  </div>
  <div class="box">
    <a
      href="https://firebasestorage.googleapis.com/v0/b/crud-d8ca2.appspot.com/o/polvo.jpeg?alt=media&token=739d40e4-9d6b-484e-937f-757694d05541"><img
        src="https://firebasestorage.googleapis.com/v0/b/crud-d8ca2.appspot.com/o/polvo.jpeg?alt=media&token=739d40e4-9d6b-484e-937f-757694d05541"
        alt="images.jpg" /></a>
  </div>
</div>
