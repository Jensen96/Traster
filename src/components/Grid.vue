<template>
    <table>
        <thead>
            <tr>
                <th 
                    v-for="key in columns"
                    :key="key.name">
                    {{ key | capitalize }}
                </th>
            </tr>
        </thead>
        <tbody>
            <tr 
                v-for="entry in allEntries"
                :key="entry.name">
            <td 
                v-for="key in columns"
                :key="key.name">
                {{entry[key]}}
            </td>
        </tr>
        </tbody>
    </table>
</template>

<script>
  export default {
    props: {
        columns: Array,
        entries: Array,
    },
    computed: {
          allEntries: function() {
            let entries = this.entries;
            return entries;
          }
    },
    filters: {
          capitalize: function(str) {
            return str.charAt(0).toUpperCase() + str.slice(1);
          }
        }
  }
</script>