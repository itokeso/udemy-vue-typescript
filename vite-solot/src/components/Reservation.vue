<script setup lang="ts">
import Card from './Card.vue';
import Badge from './Badge.vue'
</script>

<template>
    <div class="container">
        <div class="card">
            <Card class="menu-card">
                <span>Badges</span>
                <div class="badges">
                    <Badge class="vip-badge">
                        <span>VIP</span>
                    </Badge>
                    <Badge class="normal-badge">
                        <span>Normal</span>
                    </Badge>
                </div>
            </Card>
        </div>
        <Card class="reservation-card">
            <span>John Wick</span>
            <span>Badges</span>
            <Badge class="vip-badge">
                <span >VIP</span>
            </Badge>
        </Card>
        <Card class="reservation-card">
            <span>ito</span>
            <span>Badges</span>
            <Badge class="normal-badge">
                <span>Normal</span>
            </Badge>            
        </Card>
        <Card class="reservation-card">
            <span>tanaka</span>
            <span>Badges</span>
            <Badge class="vip-badge">
                <span>VIP</span>
            </Badge>
        </Card>
    </div>
</template>

<style scoped>
.container {
    display: flex;
    flex-direction: column;
    align-items: center;
}
.menu-card {
    width: 300px;
    height: 80px;
    background-color: #ccc;
    display: flex;
    flex-direction: column;
    align-items: center;
    margin-bottom: 24px;
}

.reservation-card {
    width: 400px;
    height: 60px;
    background-color: rgb(255, 212, 147);
    display: flex;
    justify-content: space-between;
    align-items: center;
    margin-bottom: 8px;
}

.vip-badge {
    background-color: #810036;
    color: white;
}

.badges {
    display: flex;
    justify-content: space-between;
    width: 60%;
}
.normal-badge {
    background-color: blue;
    color: white;
}
</style>