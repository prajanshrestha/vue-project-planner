<template>
  <div class="home">
    <h1>Home</h1>
    <post-list :posts="posts" v-if="showPosts"></post-list>
    <button @click="showPosts = !showPosts">toggle posts</button>
    <button @click="posts.pop()">delete a post</button>
  </div>
</template>

<script>
import { ref } from '@vue/reactivity';
import PostList from "../components/PostList.vue";

export default {
  name: 'Home',
  components: {
    PostList
  },
  setup() {
    const posts = ref([
      { title: "welcome to the blog", body: "Lorem ipsum dolor sit amet consectetur, adipisicing elit. Laudantium nostrum a accusamus suscipit architecto voluptatem labore inventore possimus veritatis. Dolorem aspernatur voluptatum, praesentium sapiente architecto amet voluptates nam, quaerat ex, est tempora esse beatae! Repellendus ex ipsa culpa, eius quia doloribus nam laboriosam, consequatur soluta cum, nihil eveniet? Mollitia deleniti voluptas eveniet vel doloremque officia quod asperiores! Unde nostrum, quasi, accusamus totam suscipit culpa officiis praesentium recusandae ab magnam voluptate? Delectus quae pariatur hic aliquam expedita neque sapiente et modi quisquam, ipsam porro nemo blanditiis consectetur, molestias quibusdam reiciendis. Accusamus, iusto quas porro, nihil ea at dolor ipsam, obcaecati eaque labore molestias eligendi tenetur itaque! Corrupti laboriosam explicabo, nihil delectus facere similique exercitationem odit, a adipisci, eligendi nostrum pariatur. Hic quam omnis exercitationem itaque doloribus, dolores cum inventore quasi iste temporibus nulla. Sint voluptatem laudantium non quae possimus deleniti eius dolor fugit tempore, odio quis. Rem minima aliquam sint, nihil ipsa sit quisquam perspiciatis voluptatum iusto beatae labore quos alias mollitia quo odit sapiente magnam expedita, soluta modi repellat dolorem molestias fugiat? Reiciendis, voluptate. Adipisci fuga enim nihil dolore repudiandae aperiam repellat officia tenetur ipsum dicta eius, necessitatibus ab et, accusamus nostrum unde exercitationem omnis! Sunt animi, pariatur veritatis aperiam hic expedita assumenda magnam nemo facere minima excepturi corrupti impedit optio doloremque natus placeat maiores nisi quam tempore consequuntur. Consequuntur quas odio ratione at velit! Error iure libero atque, ut hic ea at neque alias quae assumenda ex, ab, eum quaerat voluptatibus velit beatae magni fugiat! Eaque quia temporibus, quidem nobis ullam ad doloribus! Et nihil asperiores dolores itaque, aspernatur, placeat esse voluptatum rerum delectus debitis, minus animi nobis perferendis repellendus soluta! Nihil, animi? Eius delectus nam illum illo, consectetur cupiditate sed enim sapiente impedit incidunt tenetur ipsum facilis? Sunt minima corrupti amet unde tempore esse rem dolores aperiam eaque adipisci quod eos, blanditiis exercitationem autem recusandae minus aspernatur a consequatur ipsam ullam commodi dolorum tenetur. Tempore, suscipit deserunt? Cum cumque ullam rerum exercitationem sapiente doloremque tenetur quasi quos? Ipsam molestiae illo nihil dolores dolore, ipsa laborum ad obcaecati aspernatur quia eveniet voluptatibus placeat odit dolor qui quasi earum impedit tempora laboriosam. Amet porro accusamus excepturi officia fugit nisi id animi modi, sequi nihil dolorum libero delectus tenetur? Nesciunt quibusdam laboriosam illum et reiciendis quod vero accusantium quaerat error recusandae, quo alias repellat ipsum iusto, quam laudantium? Nesciunt, numquam id! Voluptates corporis veritatis similique et dolorum facilis sed quo quibusdam harum omnis placeat rerum iure consequuntur deleniti atque possimus ducimus illo, sunt molestiae magnam. Dolorum animi laborum similique? Quidem voluptatem beatae veritatis tenetur totam accusamus quae, delectus quod est vitae vero eos enim similique, voluptatum neque et natus eum! Magni, hic consequatur. Voluptatibus illum corrupti eius voluptas reprehenderit! Deserunt, quo officiis odio fugit eligendi, aut facilis esse eaque quis eveniet pariatur fuga sint? Sed blanditiis assumenda nesciunt explicabo sint error tenetur ex maxime perferendis cupiditate. Quae omnis temporibus vel neque molestias distinctio, itaque ullam dolore obcaecati vitae saepe eum ipsam quia delectus quasi odio iste eius officiis in consequuntur similique.", id: 1 },
      { title: "top 5 css tips", body: "lorem ipsum", id: 2 }
    ]);

    const showPosts = ref(true);  

    return { posts, showPosts };
  }
}
</script>
