# PaintJob
Overloaded functions that return how many buckets of paint is needed to be bought to paint a wall.


public class PaintJob {
    public static int getBucketCount (double width, double height, double areaPerBucket, int extraBuckets){
        if (width <= 0 || height <=0 || areaPerBucket <= 0 || extraBuckets < 0 ){
            return -1;
        }
        int buckets =(int)( Math.ceil((width*height/areaPerBucket))) - extraBuckets;
        return buckets;
    }
    public static int getBucketCount (double width, double height, double areaPerBucket){
        if (width <= 0 || height <=0 || areaPerBucket <= 0){
            return -1;
        }
        int buckets =(int)( Math.ceil((width*height/areaPerBucket)));
        return buckets;
    }
    public static int getBucketCount (double area, double areaPerBucket){
        if (area <= 0 || areaPerBucket <= 0){
            return -1;
        }
        int buckets =(int)( Math.ceil((area/areaPerBucket)));
        return buckets;
    }
}
