import Vue from 'vue';
import MyComponent from 'MyComponent.vue';

describe('MyComponent', () => {
    it('has a created hook', () => {
        expect(typeof MyComponent.created).toBe('function')
    })

    it('sets the correct default data', () => {
        expect(typeof MyComponent.data).toBe('function')
        const defaultData = MyComponent.data()
        expect(defaultData.message).toBe('hello')
    })

    it('correctly sets the message when created', () => {
        const vm = new Vue(MyComponent).$mount()
        expect(vm.message).toBe('Bye!')
    })

    if('renders the correct message', () => {
        const Constructor = Vue.extend(MyComponent)
        const vm = new Constructor().$mount()
        expect(vm.$el.textContent).toBe('bye!')
    })
})