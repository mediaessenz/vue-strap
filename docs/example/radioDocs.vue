<template>
  <doc-section id="radio" name="Radio">
    <div class="bs-example">
      <h4>Radio</h4>
      <radio :checked="radioValue" @checked="radioValue = arguments[0]" value="one">One</radio>
      <radio :checked="radioValue" @checked="radioValue = arguments[0]" value="two" type="danger" disabled>Two (disabled)</radio>
      <radio :checked="radioValue" @checked="radioValue = arguments[0]" value="two" type="warning" readonly>Two (readonly)</radio>
      <radio :checked="radioValue" @checked="radioValue = arguments[0]" value="two" type="success">Two</radio>
      <hr>
      <h4>Radio Button (Single buttons)</h4>
      <radio button :checked="radioValue" @checked="radioValue = arguments[0]" value="three" type="primary">Three</radio>
      <radio button :checked="radioValue" @checked="radioValue = arguments[0]" value="four" type="info" disabled>Four (disabled)</radio>
      <radio button :checked="radioValue" @checked="radioValue = arguments[0]" value="four" type="info" readonly>Four (readonly)</radio>
      <radio button :checked="radioValue" @checked="radioValue = arguments[0]" value="four" type="info">Four</radio>
      <p><pre>Radio value: {{ radioValue }}</pre></p>
    </div>
    <doc-code language="markup">
      &lt;radio :checked="radioValue" @checked="radioValue = arguments[0]" value="one">One&lt;/radio>
      &lt;radio :checked="radioValue" @checked="radioValue = arguments[0]" value="two" type="primary">Two&lt;/radio>
      &lt;radio button :checked="radioValue" @checked="radioValue = arguments[0]" value="three" type="danger">Three&lt;/radio>
      &lt;radio button :checked="radioValue" @checked="radioValue = arguments[0]" value="four" type="info">Four&lt;/radio>
    </doc-code>
    <doc-table>
      <div>
        <p>checked</p>
        <p><code>Number</code> or <code>String</code></p>
        <p></p>
        <p>Handle the selected value.</p>
      </div>
      <div>
        <p>value</p>
        <p><code>Number</code> or <code>String</code></p>
        <p></p>
        <p>Value to return if the radio item is selected.</p>
      </div>
      <div>
        <p>type</p>
        <p><code>String</code>, one of <code>default</code>
        <code>primary</code>
        <code>danger</code>
        <code>info</code>
        <code>warning</code>
        <code>success</code></p>
        <p><code>default</code></p>
        <p></p>
      </div>
      <div>
        <p>button</p>
        <p><code>Boolean</code></p>
        <p>false</p>
        <p>Button style.</p>
      </div>
    </doc-table>
    <p>See <a href="#button-group">Button Group</a> for more options.</p>
  </doc-section>
</template>

<script>
import docSection from './utils/docSection.vue'
import docTable from './utils/docTable.js'
import docCode from './utils/docCode.js'
import radio from 'src/Radio.vue'

export default {
  components: {
    docSection,
    docTable,
    docCode,
    radio
  },
  data () {
    return {
      radioValue: null
    }
  }
}
</script>
