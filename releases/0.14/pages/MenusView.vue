<template lang="pug">
  component-view(v-bind:doc="doc" id="menus-view")
</template>

<script>
  export default {
    data () {
      return {
        doc: {
          title: 'Menu',
          component: 'menu',
          edit: 'MenusView',
          desc: 'The <code>v-menu</code> component shows a menu at the position of the element used to activate it.',
          examples: [
            { header: 'Activator', file: 'menus/1', desc: 'Remember to put the element that activates the menu in the <code>activator</code> slot.' },
            { header: 'Absolute position', file: 'menus/4', desc: 'Menus can also be placed absolutely on top of the activator element using the <code>position-absolutely</code> prop. Try clicking anywhere on the image.' },
            { header: 'Absolute position without activator', file: 'menus/5', desc: 'Menus can also be used without an activator by using <code>position-absolutely</code> together with the props <code>position-x</code> and <code>position-y</code>. Try right-clicking anywhere on the image.' },
            { header: 'Hover', file: 'menus/6', desc: 'Menus can be accessed using hover instead of clicking with the <code>open-on-hover</code> prop.' },
            { header: 'Menus', file: 'menus/2', desc: 'Menus can be placed within almost any component.' },
            { header: 'Custom transitions', file: 'menus/3', desc: `Vuetify comes with 3 standard transitions, <strong>scale</strong>, <strong>slide-x</strong> and <strong>slide-y</strong>. You can also create your own and pass it as the transition argument. For an example of how the stock transitions are constructed, visit <a href="https://github.com/vuetifyjs/vuetify/blob/master/src/util/helpers.js#L13" target="_blank" rel="noopener">here</a>.` }
          ],
          props: {
            'v-menu': {
              shared: ['detachable'],
              params: [
                [
                  'full-width',
                  'Boolean',
                  'False',
                  'Changes the menu display to block, useful for filling available width in forms'
                ],
                [
                  'max-width',
                  '[Number, String]',
                  'null',
                  `Set's the maximum width for the menu content`
                ],
                [
                  'top',
                  'Boolean',
                  'False',
                  'Designates menu open up'
                ],
                [
                  'right',
                  'Boolean',
                  'False',
                  'Designates menu overflow to the right'
                ],
                [
                  'bottom',
                  'Boolean',
                  'False',
                  'Designates menu open down'
                ],
                [
                  'left',
                  'Boolean',
                  'False',
                  'Designates menu overflow to the left'
                ],
                [
                  'offset-x',
                  'Boolean',
                  'False',
                  'Offset the menu on the x-axis. Works in conjunction with direction left/right'
                ],
                [
                  'offset-y',
                  'Boolean',
                  'False',
                  'Offset the menu on the y-axis. Works in conjunction with direction top/rightbottom'
                ],
                [
                  'disabled',
                  'Boolean',
                  'False',
                  'Disables the menu'
                ],
                [
                  'max-height',
                  'Number',
                  'null',
                  'The maximum height of the menu, will overflow-y with scroll if content is too large'
                ],
                [
                  'nudge-x-auto',
                  'Number',
                  '-16',
                  'Nudge the menu on the x-axis'
                ],
                [
                  'nudge-y-auto',
                  'Number',
                  '-18',
                  'Nudge the menu on the y-axis'
                ],
                [
                  'nudge-top',
                  'Number',
                  '0',
                  'Nudge the menu from the top'
                ],
                [
                  'nudge-bottom',
                  'Number',
                  '0',
                  'Nudge the menu from the bottom'
                ],
                [
                  'nudge-left',
                  'Number',
                  '0',
                  'Nudge the menu from the left'
                ],
                [
                  'nudge-right',
                  'Number',
                  '0',
                  'Nudge the menu from the right'
                ],
                [
                  'open-on-click',
                  'Boolean',
                  'True',
                  'Designates whether menu should open on activator click'
                ],
                [
                  'close-on-click',
                  'Boolean',
                  'True',
                  'Designates if menu should close on outside-activator click'
                ],
                [
                  'origin',
                  'String',
                  'top left',
                  'Set the transform-origin of the transition'
                ],
                [
                  'transition',
                  'String',
                  'v-menu-transition',
                  'Set the transition component'
                ],
                [
                  'lazy',
                  'Boolean',
                  'False',
                  'Conditionally renders content on mounted'
                ],
                [
                  'position-x',
                  'Number',
                  '0',
                  'Used to position the menu when not using an activator slot'
                ],
                [
                  'position-y',
                  'Number',
                  '0',
                  'Used to position the menu when not using an activator slot'
                ]
              ]
            }
          },
          slots: {
            'v-menu': {
              shared: ['default'],
              params: [
                [
                  'activator',
                  'The element that will activate the menu'
                ]
              ]
            }
          },
          events: {
            'v-menu': {
              params: [
                ['activate', 'NULL', 'Menu has been activated'],
                ['deactivate', 'NULL', 'Menu has been deactivated'],
              ]
            },
          }
        }
      }
    }
  }
</script>
