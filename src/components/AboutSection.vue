<template>
    <section class="bg-white text-white mt-18" id="about">
    
        <div class="absolute z-0 top-[93rem] inset-x-0 h-64 flex items-start">
           <div class="invisible w-64 h-24 bg-gradient-to-br from bg-amber-500 via-red-700-secondary to-[#570cac] blur-2xl opacity-20"></div>
        </div>
        <div class="items-center gap-8 px-4 py-8 md:grid md:grid-cols-2 xl:gap-16 sm:py-16 xl:px-16 z-1">
            <div data-aos="flip-right">
                <h2 class="mb-8 text-4xl font-black text-left text-black">My Education</h2>
                <div class="py-8 space-y-8">
                    <div v-for="element in education" :key="element.id"
                    class="flex items-center md:w[80%] w-full rounded-xl bg-[#111a3e] shadow-lg border border-[#1f1641]">
                        <div class="w-1/4">
                            <img src="https://img.icons8.com/ios-glyphs/60/ffffff/graduation-cap--v1.png" alt="graduation-cap--v1"  />
                        </div>
                        <div class="w-3/4 pl-4">
                            <h3 class="text-2xl font-semibold text-transparent uppercase bg-clip-text bg-gradient-to-r from-yellow-500 to-red-500-400">
                                {{ element.school }}
                            </h3>
                            <p class="text-gray-400">{{ element.program }}</p>
                            <p class="text-gray-400">{{ element.year }}</p>
                        </div>
                    </div>
                </div>
            </div>
            <div class="z-10 flex flex-col h-full mt-4 text-left md:mt-0" data-aos="fade-right">
                <div v-if="$i18n.locale === 'khm'" @click="changeLanguage('khm')">
                   <h2 class="mb-4 text-4xl font-bold text-left text-black md:text-center">អំពីខ្ញុំ</h2>
                <p class="py-8 mt-8 text-black lg:text-lg">
                    ខ្ញុំឈ្មោះ រឿន សារិទ្ធ មានស្រុកកំណើតនៅខេត្តព្រៃវែង សព្វថ្ងៃជាមន្ត្រីរាជការនៅក្រសួងសុខាភិបាល ដែលមកបំរើការនៅមជ្ឃមណ្ឌលជាតិលើកកំពស់សុខភាព។
                </p> 
                    
                </div>
                <div v-else @click="changeLanguage('en')">
                <h2 class="mb-4 text-4xl font-bold text-left text-black md:text-center">About Me</h2>
                <p class="py-8 mt-8 text-black lg:text-lg">
                    I was born Prey Veng Province now day i work for Ministry of Health (Nationl Center of Health Promotion  )duration 11 year 
                    My experience befor work for goverment i work for Campany 7year Web Developer
                </p>
                </div>

                <div v-if="$i18n.locale === 'khm'" @click="changeLanguage('khm')">
                    <div class="grid max-w-lg grid-cols-3 gap-4 pt-8">
                    <div class="text-center rounded-xl bg-[#111a3e] shadow-lg border border-[#1f1641] p-3">
                        <h3 class="text-xl font-bold text-white sm:text-2xl lg:text-3xl">៥</h3>
                        <p class="text-sm text-gray-400 sm:text-base">គម្រោង</p>
                    </div>
                     <div class="text-center rounded-xl bg-[#111a3e] shadow-lg border border-[#1f1641] p-3">
                        <h3 class="text-xl font-bold text-white sm:text-2xl lg:text-3xl">៧</h3>
                        <p class="text-sm text-gray-400 sm:text-base">បទពិសោធន័ធ្វើការឯកជន</p>
                    </div>
                     <div class="text-center rounded-xl bg-[#111a3e] shadow-lg border border-[#1f1641] p-3">
                        <h3 class="text-xl font-bold text-white sm:text-2xl lg:text-3xl">១១</h3>
                        <p class="text-sm text-gray-400 sm:text-base">បទពិសោធន៍ធ្វើការរដ្ខ</p>
                    </div>
                </div>
                </div>
                <div v-else @click="changeLanguage('en')">

                <div class="grid max-w-lg grid-cols-3 gap-4 pt-8">
                    <div class="text-center rounded-xl bg-[#111a3e] shadow-lg border border-[#1f1641] p-3">
                        <h3 class="text-xl font-bold text-white sm:text-2xl lg:text-3xl">5</h3>
                        <p class="text-sm text-gray-400 sm:text-base">Work Project</p>
                    </div>
                     <div class="text-center rounded-xl bg-[#111a3e] shadow-lg border border-[#1f1641] p-3">
                        <h3 class="text-xl font-bold text-white sm:text-2xl lg:text-3xl">7</h3>
                        <p class="text-sm text-gray-400 sm:text-base">Years Experience</p>
                    </div>
                     <div class="text-center rounded-xl bg-[#111a3e] shadow-lg border border-[#1f1641] p-3">
                        <h3 class="text-xl font-bold text-white sm:text-2xl lg:text-3xl">11</h3>
                        <p class="text-sm text-gray-400 sm:text-base">Years Experience</p>
                    </div>
                </div>
                </div>
            </div>
        </div>
    </section>
</template>

<script setup>
import { ref } from 'vue';
const education = ref([
    { id: 1, school: 'Asia Erup University', program: 'Bachelor of Science in Computer Science', year: '2006 - 2009' },
    { id: 2, school: 'Messag HightSchool', program: 'Bacc II', year: '2000 - 2006' },
    { id: 3, school: 'Pusnay Primary School', program: 'Master of Audit', year: '1994 - 2000' }
])

</script>

