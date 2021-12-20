<template>
    <v-container class="my-15">
        <v-row justify="center">
            <v-col lg="12" class="text-center">
                <v-subheader class="text-h4 justify-center">Portfolio</v-subheader>
                <p>Lorem ipsum dolor sit amet consectetur adipisicing elit. Reiciendis, molestiae!</p>
            </v-col>
            <v-col lg ="12">
                <div class="text-center">
                    <v-chip @click="activePortfolio = 'webapp'" :color="activePortfolio == 'webapp'? 'success' :'' " class="mx-5">Web App</v-chip>
                    <v-chip @click="activePortfolio = 'mobileapp'" :color="activePortfolio == 'mobileapp'? 'success' :''" class="mx-5">Mobile App</v-chip>
                    <v-chip @click="activePortfolio = 'deskapp'" :color="activePortfolio == 'deskapp'? 'success' :'' " class="mx-5">Desktop App</v-chip>
                </div>
            </v-col>
           <slot v-if="activePortfolio == 'webapp'">
                <v-col lg="3" v-for="(web,webindex) in webApss" :key="webindex">
                <v-img
                    :src="web.image"
                    class="white--text align-end"
                    gradient="to bottom, rgba(0,0,0,.1), rgba(0,0,0,.5)"
                    height="200px"
                >
                    <v-card-title>{{web.title}}</v-card-title>
                </v-img>
            </v-col>
           </slot>
             <slot v-if="activePortfolio == 'mobileapp'">
                <v-col lg="3" v-for="(mobile,mobileindex) in mobileApps" :key="mobileindex">
                <v-img
                    :src="mobile.image"
                    class="white--text align-end"
                    gradient="to bottom, rgba(0,0,0,.1), rgba(0,0,0,.5)"
                    height="200px"
                >
                    <v-card-title>{{mobile.title}}</v-card-title>
                </v-img>
            </v-col>
           </slot>
            <slot v-if="activePortfolio == 'deskapp'">
                <v-col lg="3" v-for="(desk,deskeindex) in deskApps" :key="deskeindex">
                <v-img
                    :src="desk.image"
                    class="white--text align-end"
                    gradient="to bottom, rgba(0,0,0,.1), rgba(0,0,0,.5)"
                    height="200px"
                >
                    <v-card-title>{{desk.title}}</v-card-title>
                </v-img>
            </v-col>
           </slot>
        </v-row>
    </v-container>
        
    
</template>
<script>
export default {
    name: "Portfolio",
    data() {
        return {
            activePortfolio:'webapp',
            webApss:[
                {title:'Web App 1', image:'https://public-files.gumroad.com/variants/ftjzlkq38a6v1hvrkf1bdt3zsy2z/3298c3eb001bbed90f1d616da66708480096a0a1b6e81bd4f8a2d6e9b831d301'},
                {title:'Web App 2', image:"https://public-files.gumroad.com/variants/2vu17w7kwc6w5mv3k7aolued5v07/3298c3eb001bbed90f1d616da66708480096a0a1b6e81bd4f8a2d6e9b831d301"},
                {title:'Web App 3', image:"https://public-files.gumroad.com/variants/i0d2oq6sa6jzviy2t644xx1j6hq8/3298c3eb001bbed90f1d616da66708480096a0a1b6e81bd4f8a2d6e9b831d301"},
                {title:'Web App 4', image:'https://public-files.gumroad.com/variants/ftjzlkq38a6v1hvrkf1bdt3zsy2z/3298c3eb001bbed90f1d616da66708480096a0a1b6e81bd4f8a2d6e9b831d301'},
                {title:'Web App 5', image:"https://public-files.gumroad.com/variants/2vu17w7kwc6w5mv3k7aolued5v07/3298c3eb001bbed90f1d616da66708480096a0a1b6e81bd4f8a2d6e9b831d301"},
                {title:'Web App 6', image:"https://public-files.gumroad.com/variants/i0d2oq6sa6jzviy2t644xx1j6hq8/3298c3eb001bbed90f1d616da66708480096a0a1b6e81bd4f8a2d6e9b831d301"},
                {title:'Web App 7', image:'https://public-files.gumroad.com/variants/ftjzlkq38a6v1hvrkf1bdt3zsy2z/3298c3eb001bbed90f1d616da66708480096a0a1b6e81bd4f8a2d6e9b831d301'},                
            ],
            mobileApps:[
                {title:'Mobile App 1', image:'https://public-files.gumroad.com/variants/ftjzlkq38a6v1hvrkf1bdt3zsy2z/3298c3eb001bbed90f1d616da66708480096a0a1b6e81bd4f8a2d6e9b831d301'},
                {title:'Mobile App 2', image:"https://public-files.gumroad.com/variants/2vu17w7kwc6w5mv3k7aolued5v07/3298c3eb001bbed90f1d616da66708480096a0a1b6e81bd4f8a2d6e9b831d301"},
                {title:'Mobile App 3', image:"https://public-files.gumroad.com/variants/i0d2oq6sa6jzviy2t644xx1j6hq8/3298c3eb001bbed90f1d616da66708480096a0a1b6e81bd4f8a2d6e9b831d301"},
                {title:'Mobile App 4', image:'https://public-files.gumroad.com/variants/ftjzlkq38a6v1hvrkf1bdt3zsy2z/3298c3eb001bbed90f1d616da66708480096a0a1b6e81bd4f8a2d6e9b831d301'},
                {title:'Mobile App 5', image:"https://public-files.gumroad.com/variants/2vu17w7kwc6w5mv3k7aolued5v07/3298c3eb001bbed90f1d616da66708480096a0a1b6e81bd4f8a2d6e9b831d301"},
                {title:'Mobile App 6', image:"https://public-files.gumroad.com/variants/i0d2oq6sa6jzviy2t644xx1j6hq8/3298c3eb001bbed90f1d616da66708480096a0a1b6e81bd4f8a2d6e9b831d301"},
                {title:'Mobile App 7', image:'https://public-files.gumroad.com/variants/ftjzlkq38a6v1hvrkf1bdt3zsy2z/3298c3eb001bbed90f1d616da66708480096a0a1b6e81bd4f8a2d6e9b831d301'},  
            ],
            deskApps:[
                {title:'Desktop App 1', image:'https://public-files.gumroad.com/variants/ftjzlkq38a6v1hvrkf1bdt3zsy2z/3298c3eb001bbed90f1d616da66708480096a0a1b6e81bd4f8a2d6e9b831d301'},
                {title:'Desktop App 2', image:"https://public-files.gumroad.com/variants/2vu17w7kwc6w5mv3k7aolued5v07/3298c3eb001bbed90f1d616da66708480096a0a1b6e81bd4f8a2d6e9b831d301"},
                {title:'Desktop App 3', image:"https://public-files.gumroad.com/variants/i0d2oq6sa6jzviy2t644xx1j6hq8/3298c3eb001bbed90f1d616da66708480096a0a1b6e81bd4f8a2d6e9b831d301"},
                {title:'Desktop App 4', image:'https://public-files.gumroad.com/variants/ftjzlkq38a6v1hvrkf1bdt3zsy2z/3298c3eb001bbed90f1d616da66708480096a0a1b6e81bd4f8a2d6e9b831d301'},
                {title:'Desktop App 5', image:"https://public-files.gumroad.com/variants/2vu17w7kwc6w5mv3k7aolued5v07/3298c3eb001bbed90f1d616da66708480096a0a1b6e81bd4f8a2d6e9b831d301"},
                {title:'Desktop App 6', image:"https://public-files.gumroad.com/variants/i0d2oq6sa6jzviy2t644xx1j6hq8/3298c3eb001bbed90f1d616da66708480096a0a1b6e81bd4f8a2d6e9b831d301"},
                {title:'Desktop App 7', image:'https://public-files.gumroad.com/variants/ftjzlkq38a6v1hvrkf1bdt3zsy2z/3298c3eb001bbed90f1d616da66708480096a0a1b6e81bd4f8a2d6e9b831d301'},  
            ],
        }
    },
}
</script>

<style scoped>

</style>