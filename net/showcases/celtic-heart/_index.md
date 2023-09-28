---
title: "Creating Semi-transparent Celtic Heart Figure Text"
type: docs
url: /net/showcases/celtic-heart/
weight: 20
description: Creating semi-transparent Celtic Heart figure text drawing with Aspose.Drawing .NET (C#) 2d graphic library
keywords: [2d drawing,]
---

## Creating semi-transparent Celtic Heart figure text

<p align='justify'>
&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;
The first impression is crucial when introducing new content to customers or viewers. Creating splash screens or digital art objects can be accomplished more quickly and effectively with a powerful tool like the Aspose.Drawing graphic library for .NET (C#). You can leverage a variety of ready-to-use functions from the library's API for text and image drawings, manipulate graphic objects with controlled transparency levels, and blend bitmaps to craft stunning art objects.
</p>

<p align='justify'>
&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;
In our showcase example, we craft a drawing featuring Celtic rune text drawn along an intricate, curvy path that resembles a heart shape with multiple intersections. At the center of this design, we employ a 10-node knot with semi-intersections, represented by a semi-transparent ribbon. While it may appear complex initially, we'll guide you through the showcase with step-by-step C# code examples.
</p>

<p align='justify'>
&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;
Let's begin with a basic example. In the illustration below, you can observe two simple unknot paths represented by cyan and magenta circles, which are linked together, forming a structure known as the Hopf Link. These paths intersect at 2 points, or in other words, the figure comprises 2 nodes. Simultaneously, we can observe 2 ribbons (segments), with the cyan ribbon passing over the magenta ribbon at one node, and vice versa magenta over the cyan at the second node. In the second illustration, an extra node is introduced due to the self-intersection of the cyan ribbon.
</p>

<style>
   .frame {
    border: 2px solid darkgray;
    padding: 5px;
    margin: 10px 0 5px 5px;
    background: #f0f0f0;
    align-items: center;
   }
   .marginauto {
    margin: 10px auto 20px;
    display: block;
   }
   .frame figcaption {
    margin: 0 auto;
    display: flex;
    flex-direction: row;
    justify-content: center;
   }
   .container {
    display: flex;
    flex-direction: row;
    align-items: center;
    justify-content: space-around;
   }
</style>

<figure class="frame">
<div class="container">
    <div>
        <figcaption>Hopf Link</figcaption>
    </div>
    <div>
        <figcaption>Self-intersection</figcaption>
    </div>
</div>
<div class="container">
    <div>
        <img src="./hopf_link.webp" alt="Hopf Link" width="400" height="283"/>
    </div>
    <div>
        <img src="./intersection.webp" alt="Self-intersection" width="400" height="275"/>
    </div>
</div>
<figcaption>Ribbon path drawing</figcaption>
</figure>

<p align='justify'>
&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;
In our Celtic Heart showcase, we created a figure that also consists of two linked paths. The internal path is a knot with 10 nodes (and accordingly, 10 self-intersections), while the external second path resembles a large heart and has 6 intersections with the first path. In three nodes, the second path crosses above the first one, and in three other nodes, it goes below another ribbon.
</p>

<figure class="frame"><p>
    <img class="marginauto" src="./sample_CelticHeart.png" alt="Celtic Heart figure text" width="640" height="360"/>
<figcaption>Celtic Heart figure text</figcaption>
</p></figure>

<p align='justify'>
&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;
We create a `Node` object that describes the point where ribbon segments intersect. The path contains multiple alternations where the ribbon passes beneath and then above another ribbon. Therefore, each Node has one ribbon that takes the upper route and two ribbons where segments pass beneath the upper ribbon. Consequently, the `Ribbon` object has its path with three Nodes: the starting Node, where the ribbon begins from beneath an upper ribbon, the Node where the ribbon takes the upper route above another ribbon, and the ending Node, where the ribbon once again passes beneath another ribbon. Additionally, the ribbon includes its text and a list of shifts that indicate the positions, angles, and corrections (hints) for each symbol.
</p>

```cs
internal class Node
{
    public PointF Point;
    public Span? SegA;
    public Span? SegB;
    public bool Otherwise;
    public Ribbon? Ribbon1;
    public Ribbon? Ribbon2;
    public Ribbon? Ribbon3;
}

internal class Ribbon
{
    public GraphicsPath Path = new();
    public string Text = RandomString();
    public List<Shift> Shifts = new();
    public Node? Node1;
    public Node? Node2;
    public Node? Node3;
}

internal class Shift
{
    public float X;
    public float Y;
    public float Angle;
    public float Hint;

    public Shift(float x, float y, float angle, float hint)
    {
        this.X = x;
        this.Y = y;
        this.Angle = angle;
        this.Hint = hint;
    }
}
```

<p align='justify'>
&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;
Each ribbon contains a random text string composed of runic symbols. In the showcase video, these symbols move and disappear under the upper ribbon, while new symbols appear from the other side of the same ribbon segment. To achieve this effect, we randomly select runic symbols from the initial list of 52 runic symbols and add them to the string during the string shift, ensuring that the new symbol is different from its neighbor. This is accomplished by removing the neighbor symbol from the initial list once it has been selected.
</p>

```cs
private static readonly string text = "ᛦᛨᛩᛪ᛭ᛮᛯᛰᚠᛅᛆᛇᛈᛉᛊᛋᛏᛐᛒᛓᛗᛘᛚᛝᛞᛟᛠᛡᛢᛣᛥᚨᚩᚪᚫᚬᚭᚮᚯᚰᚱᚳᚴᚷᚸᚹᚺᚻᚼᚾᚿᛀ";

private static string ShiftString(string t)
{
    string text2 = text.Remove(text.IndexOf(t[0]), 1);
    int i = random.Next(0, text2.Length - 1);
    return text2[i] + t[..^1];
}

private static string RandomString()
{
    string text2 = text;
    for (int i = 0; i < text2.Length; i++)
    {
        text2 = ShiftString(text2);
    }
    return text2;
}
```

<p align='justify'>
&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;

<a href="https://reference.aspose.com/drawing/net/aspose.drawing.drawing2d/graphicspath/flatten/">GraphicsPath.Flatten</a>

<a href="https://reference.aspose.com/drawing/net/aspose.drawing.drawing2d/graphicspath/pathpoints/">GraphicsPath.PathPoints property</a>

</p>

```cs
GraphicsPath flatPath1 = (GraphicsPath)path1.Clone();
GraphicsPath flatPath2 = (GraphicsPath)path2.Clone();

flatPath1.Flatten();
flatPath2.Flatten();

List<Node> nodes = new();
List<Span> segments = new();
List<Span> segments1 = new();
List<Span> segments2 = new();

PointF[] points1 = flatPath1.PathPoints;
PointF[] points2 = flatPath2.PathPoints;

AddSpans(segments1, points1);
AddSpans(segments2, points2);
segments.AddRange(segments2);
segments.AddRange(segments1);
```

<p align='justify'>
&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;
Compare spans in segments, find intersections and fill the `nodes` list with segments' intersection
</p>

```cs
int num = 0;
for (int i = 0; i < segments.Count; i++)
{
    for (int j = i + 1; j < segments.Count; j++)
    {
        Span segA = segments[i];
        Span segB = segments[j];

        if (segA[0].Equals(segB[0]) || segA[0].Equals(segB[1]) ||
            segA[1].Equals(segB[0]) || segA[1].Equals(segB[1]))
        {
            continue;
        }

        FindIntersection(
            segA[0], segA[1], segB[0], segB[1],
            out bool segments_intersect, out PointF intersection_point);

        if (segments_intersect)
        {
            Node node = new();
            segA.Node = node;
            segB.Node = node;
            node.Point = intersection_point;
            node.SegA = segA;
            node.SegB = segB;
            node.Otherwise = num % 2 == 0;
            nodes.Add(node);
            num++;
        }
    }
}

Node last = nodes[^1];
last.Otherwise = !last.Otherwise;

List<Ribbon> ribbons = new();
MakeRibbons(ribbons, segments2);
MakeRibbons(ribbons, segments1);
CalcShifts(ribbons, g);
```

<p align='justify'>
&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;

</p>

```cs
ImageAttributes imageAttributes = new();
ColorMatrix colorMatrix = new(
    new float[][]
    {
        new float[] { 1, 0, 0, 0, 0 },
        new float[] { 0, 1, 0, 0, 0 },
        new float[] { 0, 0, 1, 0, 0 },
        new float[] { 0, 0, 0, 0.55f, 0 },
        new float[] { 0, 0, 0, 0, 1 }
    }
);
imageAttributes.SetColorMatrix(
    colorMatrix,
    ColorMatrixFlag.Default,
    ColorAdjustType.Bitmap);

float x = 1920 / 2 - w / 2;
float y = 1080 / 2 - h / 2;

PointF[] destParallelogram = new PointF[]
{
    new PointF( x, y ),
    new PointF( x + w, y ),
    new PointF( x, y + h ),
};

RectangleF rect = new(0, 0, w, h);
```

```cs
private static readonly int k = 60; // Frame number for transition from one key position
                                    // to another on the creeping line.

for (int i = 0; i < frameLimit; i++)
{
    if (i % k == 0)
    {
        ShiftRibbonStrings(ribbons);
    }

    ++frameNumber;
    g.Clear(bgColor);
    DrawRibbons(ribbons, g);
    RedrawRibbons(ribbons, segments1, segments2, g);
    Bitmap frame = Mix(bitmap, destParallelogram, rect, imageAttributes);

    string fileName = Path.Combine(outputDirectory, $"{frameNumber:d5}.png");
    frame.Save(fileName);
    Console.WriteLine(fileName);
}
```

<p align='justify'>
&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;

</p>


<p align='justify'>
&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;

<a href="https://reference.aspose.com/drawing/net/aspose.drawing/graphics/drawimage/#drawimage_4">Graphics.DrawImage</a>


</p>

### Showcase video

<p align='justify'>
&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;
Prepare frames from background video using `ffmpeg` program:
</p>

```sh
ffmpeg -i CelticHeart/RooftopClouds.mp4 ./CelticHeart/RooftopClouds_out/%%05d.png
ffmpeg -i CelticHeart/StarrySky.mp4 ./CelticHeart/StarrySky_out/%%05d.png
```

<p align='justify'>
&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;
Make video from separate frames in PNG files and add sound:
</p>

```sh
ffmpeg -framerate 30 -i ./out/%%05d.png -vcodec libx264 -pix_fmt yuv420p ./out/out.mp4
ffmpeg -i ./out/out.mp4 -i Nakarada.mp3 -map 0:v -map 1:a -c:v copy -shortest ./out/CelticHeart.mp4
```

<script type="application/ld+json">
{
    "@context": "https://schema.org/",
    "@type": "VideoObject",
    "name": "Celtic Heart figure text",
    "duration": "PT03M50S",
    "uploadDate": "2023-09-16",
    "embedUrl": "https://www.youtube.com/embed/TkCpEYy8Ong",
    "thumbnailUrl": "https://i9.ytimg.com/vi/TkCpEYy8Ong/mqdefault.jpg?sqp=CMi6oKgG-oaymwEmCMACELQB8quKqQMa8AEB-AH-CYAC0AWKAgwIABABGEkgVChlMA8=&rs=AOn4CLC4YKu2NhaS4pRGgd81tjsqPn-J1g",
    "description": "Creating semi-transparent Celtic Heart figure text drawing with Aspose.Drawing .NET (C#) 2d graphic library",
}
</script>

<iframe width="1156" height="650" src="https://www.youtube.com/embed/TkCpEYy8Ong" title="Celtic Heart" frameborder="0" allow="accelerometer; autoplay; clipboard-write; encrypted-media; gyroscope; picture-in-picture; web-share" allowfullscreen></iframe>

### Source code

You can find the full source code of the showcase in the Aspose.Drawing Github repository: <a href="https://github.com/aspose-drawing/Aspose.Drawing-for-.NET/blob/master/Examples/Showcases/Showcases/CelticHeart.cs">CelticHeart.cs</a>
