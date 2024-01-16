 public class Mathss
    {
        //فیلد
        private int r;
        private int xm;
        private int ym;
        private int xz;
        private int yz;
        private int zz;
        private int xt;
        private int yt;
        //خاصیت
        public int R
        {
            get { return r; }
            set
            {
                if (value > 0)
                {
                    r = value;
                }
            }
        }
        public int XM
        {
            get { return xm; }
            set
            {
                if (value > 0)
                {
                    xm = value;
                }
            }
        }
        public int YM
        {
            get { return ym; }
            set
            {
                if (value > 0)
                {
                    ym = value;
                }
            }
        }
        public int XZ
        {
            get { return xz; }
            set
            {
                if (value > 0)
                {
                    xz = value;

                }
            }
        }
        public int YZ
        {
            get { return yz; }
            set
            {
                if (value > 0)
                {
                    yz = value;
                }
            }
        }
        public int ZZ
        {
            get { return zz; }
            set
            {
                if (value > 0)
                {
                    zz = value;
                }
            }
        }
        public int XT
        {
            get { return xt; }
            set
            {
                if (value > 0)
                {
                    xt = value;
                }
            }
        }
        public int YT
        {
            get { return yt; }
            set
            {
                if (value > 0)
                {
                    yt = value;
                }
            }
        }
        //مخرب
        public Mathss() { }
        //سازنده
        public Mathss(int R, int XM, int YM, int XZ, int YZ, int ZZ, int XT, int YT)
        {
            r = R;
            xm = XM;
            ym = YM;
            xz = XZ;
            yz = YZ;
            zz = ZZ;
            xt = XT;
            yt = YT;
        }
        //محیط دایره
        public double Mohd()
        {
            return 2 * r * 3.14;
        }
        //مساحت دایره
        public double Masd()
        {
            return r * r * 3.14;
        }
        //محیط مستطیل
        public int Mohm()
        {
            return (xm + ym) * 2;
        }
        //مساحت مستطیل
        public int Masm()
        {
            return xm * ym;
        }
        //مساحت ذوذنقه
        public double Masz()
        {
            return (xz + yz) * zz / 2;
        }
        //محیط مثلث
        public int Moht()
        {
            return xt + xt + xt;
        }
        //مساحت مثلث
        public double Mast()
        {
            return (xt * xt) / 2;
        }
    }
    class test1
    {
        public static void Main()
        {
            //این قسمت مشخص کننده این است که کاربر چه عملیاتی میخواهد انجام دهد 
            Console.WriteLine("1) baray dayereh adad 1 ra vared konid");
            Console.WriteLine("2) baray mostatil adad 2 ra vared konid");
            Console.WriteLine("3) baray zozanagheh adad 3 ra vared konid");
            Console.WriteLine("4) baray mostatil adad 4 ra vared konid");
            Console.WriteLine("-------------------------------------------------");
            int input = Convert.ToInt32(Console.ReadLine());
            Console.WriteLine("adad shoma : " + input);
            Console.WriteLine("-------------------------------------------------");
            Mathss mh = new Mathss();
            //برای دایره
            if (input == 1)
            {
                Console.WriteLine("masaht va mohit daiereh ");
                Console.WriteLine("shoae daiere ra vared konid = ");
                int r = Convert.ToInt32(Console.ReadLine());
                Console.WriteLine("-------------------------------------------------");
                mh.R = r;
                Console.WriteLine("mohit daiere barabar = " + mh.Mohd());
                Console.WriteLine("masahat daiere barabar = " + mh.Masd());
            }
            //برای مستطیل
            else if (input == 2)
            {
                Console.WriteLine("masaht va mohit mostatil ");
                Console.WriteLine("tool mostatil ra vared konid = ");
                int xm = Convert.ToInt32(Console.ReadLine());
                Console.WriteLine("arz mostatil ra vared konid = ");
                int ym = Convert.ToInt32(Console.ReadLine());
                Console.WriteLine("-------------------------------------------------");
                mh.XM = xm;
                mh.YM = ym;
                Console.WriteLine("mohit mostatil barabar = " + mh.Mohm());
                Console.WriteLine("masahat mostatil barabar = " + mh.Masm());
            }
            //برای ذوذنقه
            else if (input == 3)
            {
                Console.WriteLine("masaht zoozanghe");
                Console.WriteLine("ghaede kochak zoozanaghe ra vared konid = ");
                int xz = Convert.ToInt32(Console.ReadLine());
                Console.WriteLine("ghaede kochak zoozanaghe ra vared konid = ");
                int yz = Convert.ToInt32(Console.ReadLine());
                Console.WriteLine("ertefa zoozanaghe ra vared konid = ");
                int zz = Convert.ToInt32(Console.ReadLine());
                Console.WriteLine("-------------------------------------------------");
                mh.XZ = xz;
                mh.YZ = yz;
                mh.ZZ = zz;
                Console.WriteLine("masahat zoozanaghe barabar = " + mh.Masz());
            }
            //برای مثلث
            else if (input == 4)
            {
                Console.WriteLine("masaht va mohit mosals motasaviolazla ");
                Console.WriteLine("zele mosalas ra vared konid = ");
                int xt = Convert.ToInt32(Console.ReadLine());
                Console.WriteLine("ertefae mosalas ra vared konid = ");
                int yt = Convert.ToInt32(Console.ReadLine());
                Console.WriteLine("-------------------------------------------------");
                mh.XT = xt;
                mh.YT = yt;
                Console.WriteLine("mohit mosalas barabar = " + mh.Moht());
                Console.WriteLine("masahat mosalas barabar = " + mh.Mast());
            }
        }
    }
}
