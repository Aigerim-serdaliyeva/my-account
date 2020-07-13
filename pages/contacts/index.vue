<template>
    <div class="section">
        <div class="container">
            <yandex-map 
                :coords="coords"
                :zoom="12"
            >
                <ymap-marker 
                    :coords="marker1.coords" 
                    :marker-id="marker1.id" 
                    :balloon="{ header: marker1.title }"
                />
                <ymap-marker 
                    :coords="marker2.coords" 
                    :marker-id="marker2.id"
                    :icon="marker2.markerIcon"
                    :hint-content="marker2.title" 
                />
            </yandex-map>
        </div>
    </div>
</template>

<script>
export default {
    data: () => ({
        coords: [
            43.238293,
            76.945465
        ],
        marker1: {
            id: '1',
            coords: [
                43.230935,
                76.933284
            ],
            title: 'Mega Park Алматы'
        },
        marker2: {
            id: '2',
            coords: [
                43.230266,
                76.947137
            ],
            title: 'Нурлы-тау',
            markerIcon: {
                layout: 'default#image',
                imageHref: '/icon-map.png',
                imageSize: [30, 30],
                imageOffset: [0, 0]
            }
        }
    })
}
</script>

<style lang="scss">
    .ymap-container {
        height: 500px;
    }

    @media (max-width: 768px) {
        .ymap-container {
            height: 400px;
        }
    }
</style>