public class BoxV2 {
		// private จะไม่สามารถเข้าถึงจาก code ที่อยู่นอก class ได้
		private double w;
		private double d;
		private double h;
		
		//setter ควบคุมการกำหนดค่า
		public void setW(double w) {
			if(w>0.0) {
				this.w = w;
			}else {
				throw new IllegalArgumentException("ค่าความกว้างจะต้องมากกว่า 0");
			}
		}
		public void setH(double h) {
			this.h = h;
		}
		public void setD(double d) {
			this.d = d;
		}
		
		//getter
		public double getW() {
			return w;
		}
		public double getH() {
			return h;
		}
		public double getD() {
			return d;
		}
		
		//คำนวณหาปริมาตร 
		public double volume() {
			return w * h * d;
		}
		
		//คำนวณหาพื้นผิว
		public double surfaceArea() {
			return (2.0 * w * h) + (2.0 * w * d) + (2.0 * d * h);
		}
		
		//constructor
		public BoxV2(double w,double h,double d) {
			setW(w);
			this.d = d;
			setH(h);
		}
		//Default Constructor 
		public BoxV2() {
			
		}
		/* ใช้สำหรับแปลงหรือแทนข้อมูลใน object ให้อยู่ในรูปของ String 
		 * เพื่อความสะดวกในการ debug หรือนำข้อมูลใน object ไปแสดงผล
		 */
		@Override 
		public String toString() { //toString ส่งค่ากลับมาเป็น string
			return String.format("width = %.2f,Height = %.2f,depth = %.2f",w,h,d);
		}
	}
