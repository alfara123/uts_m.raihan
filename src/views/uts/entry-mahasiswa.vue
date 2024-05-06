<template>
    <v-container>
        <v-row>
            <v-text-field label="NPM" variant="outlined" v-model="mhs.npm"></v-text-field>
        </v-row>
        <v-row>
            <v-text-field label="Nama" variant="outlined" v-model="mhs.nama"></v-text-field>
        </v-row>
        <v-row>
            <v-text-field label="IPK" variant="outlined" v-model="mhs.ipk"></v-text-field>
        </v-row>
        <v-row>
            <v-btn color="blue" @click="submitMahasiswa">Submit</v-btn>
        </v-row>
    </v-container>
</template>

<script lang="ts">
import { Mahasiswa } from '@/model/Mahasiswa';

export default {
    data() {
        return {
            mhs: new Mahasiswa('', '', 0)
        };
    },
    methods: {
        submitMahasiswa() {
            // Memastikan semua field terisi
            if (!this.mhs.npm || !this.mhs.nama || this.mhs.ipk === 0) {
                alert('Mohon isi semua data sebelum mengirim.');
                return; // Menghentikan eksekusi lebih lanjut jika ada field yang belum terisi
            }

            // Memeriksa validitas nilai IPK
            if (this.mhs.ipk > 4) {
                alert('IPK tidak boleh melebihi 4');
                return; // Menghentikan eksekusi jika nilai IPK tidak valid
            }

            // Jika semua kondisi terpenuhi
            alert('Data Mahasiswa ' + this.mhs.nama + ' dengan NPM ' + this.mhs.npm + ' berhasil disimpan');
            this.mhs = new Mahasiswa('', '', 0); // Reset form
        }
    }
}
</script>


