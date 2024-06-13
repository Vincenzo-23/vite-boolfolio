<template>
    <div class="container">
        <h1 class="text-center py-3">I miei progetti</h1>
    </div>
    <div class="container mt-5">
        <ul class="row g-4">
            <li v-for="project in projects" :key="project.id" class="col-4">
                <div class="card">
                    <div class="card-body">
                        <h5 class="card-title fw-bold mb-3">{{project.title}}</h5>
                        <p class="fst-italic">{{project.type.name}}</p>
                        <ul class="card-subtitle mb-2 d-flex gap-3 py-1">
                            <li v-for="technology in project.technologies" class="tag">
                                {{technology.name}}
                            </li>
                        </ul>
                        <p class="card-text">{{project.description}}</p>
                        <a :href="project.link" class="card-link">Link alla repository</a>
                    </div>
                </div>
            </li>
        </ul>
    </div>
</template>

<script>

import axios from 'axios';

export default {
        data() {
            return {
                projects: [],
            }
        },
        methods: {
            fetchProjects() {
                axios.get('http://127.0.0.1:8000/api/projects').then(res => {
                    this.projects = res.data.projects
                })
            }
        },
        created(){
            this.fetchProjects()
        },
    }
</script>

<style lang="scss" scoped>
    .card{
        height: 100%;
        .tag{
            background-color: rgb(236, 211, 69);
            border-radius: 99px;
            padding: 2px 10px;
            font-weight: 500;
        }
    }
</style>