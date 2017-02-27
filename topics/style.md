


? so stroke, how does it work in terms of exact pixels, width or 2*width, does it depend on rendere?



    - pushStyle()
    - popStyle()


>The style information controlled by the following functions are included in the style: fill(), stroke(), tint(), strokeWeight(), strokeCap(), strokeJoin(), imageMode(), rectMode(), ellipseMode(), shapeMode(), colorMode(), textAlign(), textFont(), textMode(), textSize(), textLeading(), emissive(), specular(), shininess(), ambient() 


PStyle Class
------------

Has no methods, only fields!

figure out why many of these same fields are in PApplet and/or PGraphics, but it seems some aren't e.g. blendMode?

#### PStyle fields

    float ambientB
    float ambientG
    float ambientR
    
    int blendMode
    
    int colorMode
    float colorModeA
    float colorModeX
    float colorModeY
    float colorModeZ
    
    int ellipseMode
    
    float emissiveB
    float emissiveG
    float emissiveR
    
    boolean fill
    int fillColor
    
    int imageMode
    int rectMode
    int shapeMode
    
    float shininess
    float specularB
    float specularG
    float specularR
    
    boolean stroke
    int strokeCap
    int strokeColor
    int strokeJoin
    float strokeWeight
    int textAlign
    int textAlignY
    PFont textFont
    float textLeading
    int textMode
    float textSize
    boolean tint
    int tintColor
