<script lang="ts">
  import { type Drawing } from '@hcengineering/attachment'
  import core, { DateRangeMode } from '@hcengineering/core'
  import { DatePresenter, IconScribble } from '@hcengineering/ui'
  import { ObjectPresenter } from '@hcengineering/view-resources'

  export let value: Drawing
</script>

<div class="flex-presenter flex-gap-3">
  <DatePresenter value={value.createdOn} mode={DateRangeMode.DATETIME} kind="list" icon={IconScribble} />
  <ObjectPresenter objectId={value.createdBy} _class={core.class.Account} shouldShowName={false} />
</div>
