<template>
  <!--PanelItem :field="field" :index="index">
    <template #value>
      <div v-if="field.showAsList">
        <div class="relative rounded-lg bg-white shadow border border-60">
          <div class="overflow-hidden rounded-b-lg rounded-t-lg">
            <div class="border-b border-50 cursor-text font-mono text-sm py-2 px-4"
                 v-for="(resource, key) in field.value"
                 :key="key">
              <Link
                @click.stop
                :href="$url(`/resources/${field.resourceNameRelationship}/${resource.id}`)"
                class="link-default"
                v-if="field.viewable"
              >{{get(resource, field.optionsLabel)}}
              </Link>
              <span v-else>{{get(resource, field.optionsLabel)}}</span>
            </div>
          </div>
        </div>
      </div>
      <div v-else>
      <span v-for="(resource, key) in field.value" class="single">
        <Link
          @click.stop
          :href="$url(`/resources/${field.resourceNameRelationship}/${resource.id}`)"
          class="link-default"
          v-if="field.viewable"
        >{{get(resource, field.optionsLabel)}}</Link>
        <span v-else>{{get(resource, field.optionsLabel)}}</span>
      </span>
      </div>
    </template>
  </PanelItem-->
</template>

<script>
  export default {
    props: ["index", "resource", "resourceName", "resourceId", "field"],
    methods: {
      get(object, path, defaultValue) {
        //return _.get(object, path, defaultValue);
      }
    },
  };
</script>

<style lang="scss" scoped>
  .single:not(:last-of-type) {
    &:after {
      content: ', ';
    }
  }
</style>
