<script setup>
import { faker } from '@faker-js/faker'
import { RouterLink } from 'vue-router'
const foodname = faker.food.dish()
const food_description = faker.food.description()
const ingredients = faker.food.ingredient()
const category = faker.food.ethnicCategory()
const food_about = faker.lorem.lines(2)
const firstname = faker.person.firstName()
const lastname = faker.person.lastName()
const username = faker.internet.userName({firstName: firstname, lastName: lastname}).toLowerCase()

</script>

<template>
    <!-- {{ foodname }} <br /> -->
      <RouterLink :to="{name: 'CardDetails', params: {id: foodname}}">
      <div class="border border-gray-400 rounded-lg shadow bg-gray-200 h-full">
        <img :src="faker.image.urlLoremFlickr({category: 'food', width: 640, height: 480})" class="rounded-t-xl"/>
        <div class="p-4">
            <p class="mg-2 text-2xl font-bold">Food Name: </p>
            <p class="mb-3 text-xl font-bold text-gray-600">{{ foodname }}</p>
            <p class="mg-2 text-2xl font-bold">Food Description: </p>
            <p class="mb-3 text-xl font-bold text-gray-600">{{ food_description }}</p>
            <p class="mg-2 text-2xl font-bold">Ingredients: </p>
            <p class="mb-3 text-xl font-bold text-gray-600">{{ ingredients }}</p>
            <p class="mg-2 text-2xl font-bold">Category: </p>
            <p class="mb-3 text-xl font-bold text-gray-600">{{ category }}</p>
            <p class="mg-2 text-2xl font-bold">About the Food: </p>
            <p class="mb-3 text-xl font-bold text-gray-600">{{ food_about }}</p>
        </div>
      </div>
      </RouterLink>
</template>