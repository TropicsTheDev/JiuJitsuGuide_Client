<template>
  <Tutorial />
</template>

<script>
import gql from "graphql-tag"

const TEST_RICK_AND_MORTY_QUERY = gql`
  query {
    characters {
      info {
        count
      }
      results {
        name
        status
        species
      }
    }
    location(id: 1) {
      id
    }
    episodesByIds(ids: [1, 2]) {
      id
    }
  }
`
export default {
  apollo: {
    characters: TEST_RICK_AND_MORTY_QUERY,
    location: TEST_RICK_AND_MORTY_QUERY,
  },
}
</script>
