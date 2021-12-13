<template>
<div class="post">
<header class="header">
 <div class="header-author">

    <avatar :size="40"/>
    <div class="header-author-info">
<div><CustomText tag="b">eraybulut34</CustomText></div>
<div><CustomText tag="span" size="xsmall">Paris, France</CustomText></div>

    </div>
 </div>
<div class="header-more"></div>
<button type="button">
<IconMore/>
</button>
</header>



<div class="post-media">
  <img src="https://avatars.mds.yandex.net/i?id=9b64e627be586b02e939dff7f7adbfec-5584150-images-thumbs&n=13" alt="">
</div>

<div class="action-buttons">
  <button type="button">
<IconLike/>
</button>
<button type="button">
<IconComment/>
</button>
<button type="button">
<IconDirect/></button>
<button type="button" class="action-save">
<IconSave />
</button>
</div>

</div>
</template>

<script>
const { default: Avatar }=require("./Avatar.vue")
import IconMore from '@/icons/more.svg'
import IconLike from '@/icons/like.svg'
import IconComment from '@/icons/comment.svg'
import IconDirect from '@/icons/direct.svg'
import IconSave from '@/icons/save.svg'
import CustomText from '@/components/CustomText'

export default {
  components: { Avatar, IconMore, IconLike,IconComment,IconDirect,IconSave,CustomText }, 
  name: 'Post',

}
</script>

<style scoped>
.post{
border-radius: 3px;
border: 1px solid rgb(var(--b6a));
max-width: 28rem;
margin-bottom: 3rem;


@media (--t){
    @media (--t) {
    display: grid;
    align-items: center;
    }
}
}
.header{
  height: 4rem;
  display: flex;
  align-items: center;
  padding-left: 1rem;
padding-right: 1rem;
  &-author{
  display: flex;
  align-items: center;
&-info{
  margin-left: 0.25rem;
}

  }
  &-more{
margin-left: auto;
  }
}
button{
  margin-left: 0.3rem;
}

.action-buttons{
  height: 3rem;
  display: flex;
  align-items: center;
  padding-left: 1rem;
padding-right: 1rem;


}

.action-save{
  margin-left: auto;
  margin-right: 0px;
}

</style>
