<template>
  <div
    class="mx-3 mt-8 px-5 pt-6 pb-1 lg:pt-10 lg:px-10 bg-indigo-50 rounded-md"
  >
    <p class="text-3xl mb-8">💿 收录列表</p>
    <div>
      <WorskListItem
        v-for="work in works"
        :key="work.id"
        :title="work.title"
        :image="work.image"
        :artist="work.artist"
        :DBs="work.DBs"
        :sheets="work.sheets"
        :updated="work.updated"
        :progress="work.progress"
        :contents="work.contents"
        :contributors="work.contributors"
      />
    </div>
  </div>
</template>

<script>
import WorskListItem from "./WorksListItem.vue";
export default {
  components: { WorskListItem },
  data() {
    return {
      works: [
        {
          id: "1",
          title: "FELT Music Collection 1.2",
          image:
            "https://ae01.alicdn.com/kf/Hbf22b9ea8e514fd6a388854c579ccd51i.jpg",
          artist: {
            name: "FELT",
            avatar:
              "https://ae01.alicdn.com/kf/H4de3975facc54155963c9b066b3f11d6X.png",
          },
          updated: "2020-07-25",
          progress: "100%",
          contents: [
            { name: "CD", total: 30, progress: 30 },
            { name: "Booklet", total: 30, progress: 30 },
            { name: "Special Content", total: 55, progress: 55 },
          ],
          DBs: [
            { name: "VGMdb", url: "https://vgmdb.net/org/746", icon: "" },
            { name: "THWiki", url: "https://thwiki.cc/FELT", icon: "" },
            {
              name: "MusicBrainz",
              url:
                "https://musicbrainz.org/artist/174596bf-3906-49a9-a448-bc1c17092634",
              icon: "",
            },
          ],
          sheets: [
            {
              name: "Google Sheet",
              url:
                "https://docs.google.com/spreadsheets/d/1tLqMgeZ8IMF5fRuE71QYCHTMDW38Oapj_gYjh5sNwyA/edit?usp=sharing",
            },
          ],
          contributors: [
            {
              avatar:
                "https://ae01.alicdn.com/kf/Hd0e601f28fbb44c88e3267308838183f3.jpg",
              name: "ame",
            },
            {
              avatar:
                "https://ae01.alicdn.com/kf/H7567cc51653b4d969d4fd16ff223978c5.jpg",
              name: "月影清风",
            },
          ],
        },
        {
          id: "2",
          title: "凋叶棕 RD-Sounds Collection 1.0",
          image:
            "https://ae01.alicdn.com/kf/H7fef35134f4a47229b44460363060983p.jpg",
          artist: {
            name: "凋叶棕",
            avatar:
              "https://ae01.alicdn.com/kf/H8ccaefb993f44367a886064e126c326bq.jpg",
          },
          contents: [
            { name: "CD", total: 35, progress: 33 },
            { name: "Booklet", total: 35, progress: 33 },
          ],
          DBs: [
            { name: "VGMdb", url: "https://vgmdb.net/org/806", icon: "" },
            { name: "THWiki", url: "https://thwiki.cc/凋叶棕", icon: "" },
            {
              name: "MusicBrainz",
              url:
                "https://musicbrainz.org/artist/731dbf08-10c3-4252-9f76-c3989719295c",
              icon: "",
            },
          ],
          sheets: [
            {
              name: "Google Sheet",
              url:
                "https://docs.google.com/spreadsheets/d/1P2SXQmIGDE1l890wv38IHFY5Io_mwgve1S6tBJ7aayQ/edit?usp=sharing",
            },
          ],

          updated: "2021-05-30",
          progress: "94%",
          contributors: [
            {
              avatar:
                "https://ae01.alicdn.com/kf/Hd0e601f28fbb44c88e3267308838183f3.jpg",
              name: "ame",
            },
          ],
        },
      ],
    };
  },
};
</script>

<style>
</style>