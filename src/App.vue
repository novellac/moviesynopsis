<template>
  <BaseRadioGroup
    legend="What's your current shirt colour?"
    groupName="shirts"
    :options="shirts"
    @update:model-value="
      inputOne = shirts.find((el) => el.value === $event).meaning
    "
  />

  <BaseRadioGroup
    legend="What beverage are you drinking?"
    groupName="beverages"
    :options="beverages"
    @update:model-value="
      inputTwo = beverages.find((el) => el.value === $event).meaning
    "
  />

  <BaseRadioGroup
    legend="First letter of the last person you texted"
    groupName="textees"
    :options="textees"
    @update:model-value="
      inputThree = textees.find((el) => el.value === $event).meaning
    "
  />

  <BaseRadioGroup
    legend="First letter of the last thing you ate"
    groupName="entrees"
    :options="entrees"
    @update:model-value="
      inputFour = entrees.find((el) => el.value === $event).meaning
    "
  />

  <Synopsis
    :one="inputOne"
    :two="inputTwo"
    :three="inputThree"
    :four="inputFour"
  />
</template>

<script>
import BaseRadioGroup from "./components/BaseRadioGroup.vue";
import Synopsis from "./components/Synopsis.vue";

import { ref } from "vue";

export default {
  name: "App",
  components: {
    BaseRadioGroup,
    Synopsis
  },
  data() {
    return {
      myInput: "bloop"
    };
  },
  setup() {
    const inputOne = ref(undefined);
    const shirts = [
      {
        value: "red",
        label: "Red",
        meaning: "An orphaned"
      },
      {
        value: "orange",
        label: "Orange",
        meaning: "A fashionably late"
      },
      {
        value: "yellow",
        label: "Yellow",
        meaning: "A manic pixie"
      },
      {
        value: "green",
        label: "Green",
        meaning: "A soul-searching"
      },
      {
        value: "blue",
        label: "Blue",
        meaning: "An unlucky-in-love"
      }
    ];

    const inputTwo = ref(undefined);
    const beverages = [
      {
        value: "coffee",
        label: "Coffee",
        meaning: "corporate lawyer"
      },
      {
        value: "tea",
        label: "Tea",
        meaning: "librarian"
      },
      {
        value: "hotchocolate",
        label: "Hot chocolate",
        meaning: "former beauty queen"
      },
      {
        value: "theraflu",
        label: "Theraflu",
        meaning: "therapist"
      },
      {
        value: "hotapplecider",
        label: "Hot apple cider",
        meaning: "paleontologist"
      }
    ];

    const inputThree = ref(undefined);
    const textees = [
      {
        value: "a",
        label: "A",
        meaning: "foreclose on a small country inn"
      },
      {
        value: "b",
        label: "B",
        meaning: "celebrate her two friends finally opening an inn"
      },
      {
        value: "c",
        label: "C",
        meaning: "settle her parents' estate"
      },
      {
        value: "d",
        label: "D",
        meaning: "teach a winter class at the community college"
      }
    ];

    const inputFour = ref(undefined);
    const entrees = [
      {
        value: "a",
        label: "A",
        meaning: "the town drunk"
      },
      {
        value: "b",
        label: "B",
        meaning: "the widowed town librarian"
      },
      {
        value: "c",
        label: "C",
        meaning: "Santa Claus"
      },
      {
        value: "d",
        label: "D",
        meaning: "her childhood crush"
      }
    ];

    return {
      shirts,
      inputOne,

      beverages,
      inputTwo,

      textees,
      inputThree,

      entrees,
      inputFour
    };
  }
};
</script>
