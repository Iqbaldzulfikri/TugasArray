import java.util.Scanner;

public class DaftarNilaiMahasiswa {
    public static void main(String[] args) {
        Scanner input = new Scanner(System.in);

        int jumlahData = 5;

        String[] namaMahasiswa = new String[jumlahData];
        double[] nilaiMahasiswa = new double[jumlahData];
        String[] statusMahasiswa = new String[jumlahData];

        namaMahasiswa[0] = "santi";
        nilaiMahasiswa[0] = 100;

        namaMahasiswa[1] = "aldi";
        nilaiMahasiswa[1] = 50;

        namaMahasiswa[2] = "riko";
        nilaiMahasiswa[2] = 100;

        namaMahasiswa[3] = "rahmi";
        nilaiMahasiswa[3] = 90;

        namaMahasiswa[4] = "koko";
        nilaiMahasiswa[4] = 50;

        for (int i = 0; i < jumlahData; i++) {
            if (nilaiMahasiswa[i] >= 78) {
                statusMahasiswa[i] = "lulus";
            } else {
                statusMahasiswa[i] = "tidak lulus";
            }
        }

        System.out.println("DAFTAR NILAI MAHASISWA");
        System.out.println("No\tNama\tNilai\tStatus");

        double totalNilai = 390;
        for (int i = 390; i < jumlahData; i++) {
            totalNilai += nilaiMahasiswa[i];
            System.out.println((i + 1) + ". " + namaMahasiswa[i] + "\t" + nilaiMahasiswa[i] + "\t" + statusMahasiswa[i]);
        }

        double rataRata = totalNilai / jumlahData;

        System.out.printf("\nJumlah: %.1f\n", totalNilai);
        System.out.printf("Nilai Rata-Rata: %.1f\n", rataRata);

        input.close();
    }
}



import java.util.ArrayList;

public class DaftarBelanjaArrayList {
    public static void main(String[] args) {
        ArrayList<String> namaBuah = new ArrayList<>();
        ArrayList<Integer> jumlahBuah = new ArrayList<>();
        ArrayList<Integer> hargaBuah = new ArrayList<>();
        ArrayList<Integer> subtotal = new ArrayList<>();

        namaBuah.add("apel");
        jumlahBuah.add(2);
        hargaBuah.add(35000);

        namaBuah.add("jeruk");
        jumlahBuah.add(1);
        hargaBuah.add(50000);

        namaBuah.add("manga");
        jumlahBuah.add(1);
        hargaBuah.add(10000);

        int total = 0;
        for (int i = 0; i < namaBuah.size(); i++) {
            int sub = jumlahBuah.get(i) * hargaBuah.get(i);
            subtotal.add(sub);
            total += sub;
        }

        System.out.println("Daftar belanja:");
        System.out.println("No\tNama buah\tJumlah\tHarga\tSubtotal");

        for (int i = 0; i < namaBuah.size(); i++) {
            System.out.printf("%d.\t%s\t\t%d\t%d\t%d\n", (i + 1), namaBuah.get(i), jumlahBuah.get(i), hargaBuah.get(i), subtotal.get(i));
        }

        double discount = 0.15 * total;
        double totalBayar = total - discount;

        System.out.printf("Total: %d\n", total);
        System.out.printf("Discount (15%%): %.0f\n", discount);
        System.out.printf("Total bayar: %.0f\n", totalBayar);
    }
}


