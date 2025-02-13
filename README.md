using System;

class Rectangle
{
    private double width;
    private double height;

    public Rectangle()
    {
        width = 1.0;
        height = 1.0;
    }

    public Rectangle(double size)
    {
        width = size;
        height = size;
    }

    public Rectangle(double width, double height)
    {
        this.width = width;
        this.height = height;
    }

    ~Rectangle()
    {
        Console.WriteLine("Прямоугольник удален");
    }

    public double Area()
    {
        return width * height;
    }

    public double Width { get; set; }
    public double Height { get; set; }
}

class Program
{
    static void Main(string[] args)
    {
        Rectangle rectangle1 = new Rectangle(5, 10);
        Console.WriteLine($"Площадь прямоугольника: {rectangle1.Area()}");

        Rectangle rectangle2 = new Rectangle(4);
        Console.WriteLine($"Площадь квадрата: {rectangle2.Area()}");

        Rectangle rectangle3 = new Rectangle();
        Console.WriteLine($"Площадь прямоугольника по умолчанию: {rectangle3.Area()}");
    }
}
