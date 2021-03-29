# PBOFS112B-2014436267-Latihan55

/*
 * To change this license header, choose License Headers in Project Properties.
 * To change this template file, choose Tools | Templates
 * and open the template in the editor.
 */

/**
 *
 * @author ASUS
 * Nama     : Caterina Vinanti
 * Kelas    : PBO FS112B
 * NIM      : 2014436267
 * Deskripsi Program : Program ini berisi tentang program Handphone
 */


class Handphone{
    String manufacture, operatingSystem, model;
    int harga;
    
    Handphone(String man, String os, String model, int harga) {
        this.manufacture = man;
        this.operatingSystem = os;
        this.model = model;
        this.harga = harga;
    }
    
    void displayProduct() {
        System.out.println("Manufaktur : " + this.manufacture);
        System.out.println("OS : " + this.operatingSystem);
        System.out.println("Model : " + this.model);
        System.out.println("Harga : " + this.harga);
    }
}

class Android {
    String keyStore;
    Handphone hp;
    
    Android(String man, String os, String model, int harga) {
    }
    
    String getKeyStore() {
        return this.keyStore;
    }
    
    void setKeyStore(String keyStore) {
        this.keyStore = keyStore;
    }
}

class BlackBerry {
    String pinBB;
    Handphone hp;
    
    BlackBerry(String man, String os, String model, int harga) {
    }
    
    String getPinBB() {
        return this.pinBB;
    }
    
    void setPinBB(String pinBB) {
        this.pinBB = pinBB;
    }
}

class WindowsPhone {
    String wpKeyStore;
    Handphone hp;
    
    WindowsPhone(String man, String os, String model, int harga) {
    }
    
    String getWpKeyStore() {
        return this.wpKeyStore;
    }
    
    void setWpKeyStore(String wpKeyStore) {
        this.wpKeyStore = wpKeyStore;
    }
}

/**
 *
 * @author eLx
 */
public class PBOFS112B_2014436267_Latihan55_Handphone {

    /**
     * @param args the command line arguments
     */
    public static void main(String[] args) {
        // TODO code application logic here
        Handphone hp1 = new Handphone("Samsung", "Android", "Grand", 3000000);
        Android android = new Android(hp1.manufacture, hp1.operatingSystem, hp1.model, hp1.harga);
        android.setKeyStore("Android_key_store");
        hp1.displayProduct();
        System.out.println("Android Key Store : " + android.getKeyStore());
        System.out.println("");
        Handphone hp2 = new Handphone("BlackBerry", "RIM", "Curve", 2000000);
        BlackBerry blackberry = new BlackBerry(hp2.manufacture, hp2.operatingSystem, hp2.model, hp2.harga);
        blackberry.setPinBB("BHS249");
        hp2.displayProduct();
        System.out.println("PIN : " + blackberry.getPinBB());
        System.out.println("");
        Handphone hp3 = new Handphone("Nokia", "Win8", "Lumia", 1000000);
        WindowsPhone wp = new WindowsPhone(hp3.manufacture, hp3.operatingSystem, hp3.model, hp3.harga);
        wp.setWpKeyStore("Windows_key_store");
        hp3.displayProduct();
        System.out.println("Wp Key Store : " + wp.getWpKeyStore());
    }
    
}

