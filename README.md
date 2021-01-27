# CompositonChallenge
package academy.learnprogrmming;

import java.util.List;

public class Main {

    static class Lamp {
        private String style;
        private boolean battery;
        private int globRating;

        public Lamp(String style, boolean battery, int globRating) {
            this.battery = battery;
            this.globRating = globRating;
            this.style = style;
        }

        public void turnOn() {
            System.out.println("Lamp -> Turning on");
        }

        public String getStyle() {
            return style;
        }

        public boolean isBattery() {
            return battery;
        }

        public int getGlobRating() {
            return globRating;
        }
    }

    static class Bed {
        private String style;
        int pillows, height, sheets, quilt;

        public Bed(String style, int pillows, int height, int sheets, int quilt) {
            this.height = height;
            this.pillows = pillows;
            this.quilt = quilt;
            this.sheets = sheets;
            this.style = style;
        }

        public void make() {
            System.out.println("Bed -> Making | ");
        }

        public int getHeight() {
            return height;
        }

        public String getStyle() {
            return style;
        }

        public int getPillows() {
            return pillows;
        }

        public int getSheets() {
            return sheets;
        }

        public int getQuilt() {
            return quilt;
        }
    }

    static class Ceiling {
        private int height;
        private int paintedColor;

        public Ceiling(int height, int paintedColor) {
            this.height = height;
            this.paintedColor = paintedColor;
        }

        public int getHeight() {
            return height;
        }

        public int getPaintedColor() {
            return paintedColor;
        }
    }

    static class Wall {
        private String direction;

        public Wall(String direction) {
            this.direction = direction;
        }

        public String getDirection() {
            return direction;
        }
    }

    static class Bedroom {
        String name;
        Wall wall1, wall2, wall3, wall4;
        Ceiling ceiling;
        Bed bed;
        Lamp lamp;

        public Bedroom(String name, Wall wall1, Wall wall2, Wall wall3, Wall wall4, Ceiling ceiling, Bed bed, Lamp lamp) {
            this.name = name;
            this.wall1 = wall1;
            this.wall2 = wall2;
            this.wall3 = wall3;
            this.wall4 = wall4;
            this.ceiling = ceiling;
            this.bed = bed;
            this.lamp = lamp;
        }

        public Lamp getLamp() {
            return lamp;
        }

        public void makeBed() {
            System.out.println("Bedroom -> Making bed | ");
            bed.make();
        }
    }

    public static void main(String[] args) {

        Wall wall1 = new Wall("west");
        Wall wall2 = new Wall("East");
        Wall wall3 = new Wall("South");
        Wall wall4 = new Wall("North");

        Ceiling ceiling = new Ceiling(12, 55);

        Bed bed = new Bed("Modern", 4, 3, 2, 1);

        Lamp lamp = new Lamp("Classic", false, 75);

        Bedroom bedroom = new Bedroom("Bilaal", wall1, wall2, wall3, wall4, ceiling, bed, lamp);
        bedroom.makeBed();

        bedroom.getLamp().turnOn();

    }
}
"C:\Program Files\Java\jdk-15.0.1\bin\java.exe" "-javaagent:C:\Users\nadiy\OneDrive\Desktop\IntelliJ IDEA Community Edition 2020.2.3\lib\idea_rt.jar=52119:C:\Users\nadiy\OneDrive\Desktop\IntelliJ IDEA Community Edition 2020.2.3\bin" -Dfile.encoding=UTF-8 -classpath C:\Users\nadiy\IdeaProjects\CompostionChallenge\out\production\CompostionChallenge academy.learnprogrmming.Main
Bedroom -> Making bed | 
Bed -> Making | 
Lamp -> Turning on

Process finished with exit code 0
