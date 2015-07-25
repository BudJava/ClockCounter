public class BoundedCounter {

    private int value;
    private int upperLimit;

    public BoundedCounter(int upperLimit) {
        this.upperLimit = upperLimit;
        this.value = 0;
    }

    public void next() {
        this.value++;
        if (this.value > upperLimit) {
            this.value = 0;
        }
    }

    public String toString() {
        int start = 0;
        if (this.value < 10) {
            return "Time: " + start + this.value;
        } else {
            return "Time: " + this.value;
        }
    }

    public int getValue() {
        return this.value;

    }

    public void setValue(int set) {

        if ((set > 0) || set > upperLimit) {
            this.value = set;
        }

    }
}


