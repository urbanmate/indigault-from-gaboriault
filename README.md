# indigault-from-gaboriault
float x = 150 ; 
float angle = 90 ;
float y = 345;
float oh = 10 ;
void setup () { 
  
  size (700,700); 

} 

void draw () { 

 background (0); 
  
  translate ( width /2 , height /2 ); 
  rotate (radians (angle)); 

  for (float a=0; a<360; a+=10) {
  
 
  
  
    pushMatrix (); 
     if (angle<360) rotate (radians (a)*sin(radians(angle))); 
   else  rotate (radians (a)); 
   
    stroke (64,0,254,155); 
    strokeWeight (2); 
    line ( x*sin ( radians(angle*3 )), x, x ,y); 
 
    
    
    stroke (64,0,254,255); 
    noFill();
  //  fill (255); 
    ellipse ( x*sin(radians(angle)), 0, oh/2, oh/2 ); 
   
   
   stroke (64,0,254,255); 
   noFill();
   // fill(255); 
    ellipse(0,y, oh,oh ); 
    popMatrix ();
  }
  angle ++ ; 
  
  
  
  
  saveFrame("indigault720/####.png"); 
  if ( angle>720) exit (); 
}
