<template>
    <BaseButton outline size="lg" w-full @click="isOpenModal = true"> open / close Modal</BaseButton>
    <BaseModal v-model="isOpenModal">
        <h1>sds</h1>
        <template #footer>
            <BaseButton outline> register</BaseButton>
        </template>
    </BaseModal>
  <ShopShowMore height="60">
    لورم ایپسوم متن ساختگی با تولید سادگی نامفهوم از صنعت چاپ، و با استفاده از طراحان گرافیک است، چاپگرها و متون بلکه روزنامه و مجله در ستون و سطرآنچنان که لازم است، و برای شرایط فعلی تکنولوژی مورد نیاز، و کاربردهای متنوع با هدف بهبود ابزارهای کاربردی می باشد، کتابهای زیادی در شصت و سه درصد گذشته حال و آینده، شناخت فراوان جامعه و متخصصان را می طلبد، تا با نرم افزارها شناخت بیشتری را برای طراحان رایانه ای علی الخصوص طراحان خلاقی، و فرهنگ پیشرو در زبان فارسی ایجاد کرد، در این صورت می توان امید داشت که تمام و دشواری موجود در ارائه راهکارها، و شرایط سخت تایپ به پایان رسد و زمان مورد نیاز شامل حروفچینی دستاوردهای اصلی، و جوابگوی سوالات پیوسته اهل دنیای موجود طراحی اساسا مورد استفاده قرار گیرد.
  </ShopShowMore>
  <Form :validation-schema="fromSchema" >
  <BaseInput name="email" v-model="email" label="ایمیل" />


</Form>
</template>

<script setup lang="ts">
import * as Yup from 'yup';
import {Form} from 'vee-validate';

    const isOpenModal = ref(false);
    const email = ref("");
    const fromSchema = Yup.object().shape({

      email:Yup.string().email().required(),
    })
</script>