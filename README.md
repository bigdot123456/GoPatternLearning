#   G o � �!j_���� 
  
 �S� 
  
 -   [ g i t h u b . c o m / s e n g h o o / g o l & ] ( h t t p s : / / g i t h u b . c o m / s e n g h o o / g o l a n g - d e s i g n - p a t t e r n )  
 -   [ g i t h u b . c o m / y k s z / g o - d e s & ] ( h t t p s : / / g i t h u b . c o m / y k s z / g o - d e s i g n - p a t t e r n s )  
 -   [ g i t h u b . c o m / s v e t t / g o l a n & ] ( h t t p s : / / g i t h u b . c o m / s v e t t / g o l a n g - d e s i g n - p a t t e r n s )  
  
 # #   s i m p l e f a c t o r y  
  
 �[g o l a n g eg�1\/fN e w x x �Qpe�ԏ�Vi n t e r f a c e �  k u b e r n e t e s   i n t e r f a c e ��Y�S����S�N���(ui n t e r f a c e �ba��v1\/fi n t e r f a c e ����O>N N*N�OP[ 
  
 ` ` `  
 / /   k 8 s . i o / k u b e r n e t e s / v e n d o r / k 8 s . i o / c l i e n t - g o / t o o l s / c a c h e / s t o r e . g o  
 f u n c   N e w S t o r e ( k e y F u n c   K e y F u n c )   S t o r e   {  
         r e t u r n   & c a c h e {  
                 c a c h e S t o r a g e :   N e w T h r e a d S a f e S t o r e ( I n d e x e r s { } ,   I n d i c e s { } ) ,  
                 k e y F u n c :             k e y F u n c ,  
         }  
 }  
  
 t y p e   c a c h e   s t r u c t   {  
         / /   c a c h e S t o r a g e   b e a r s   t h e   b u r d e n   o f   t h r e a d   s a f e t y   f o r   t h e   c a c h e  
         c a c h e S t o r a g e   T h r e a d S a f e S t o r e  
         / /   k e y F u n c   i s   u s e d   t o   m a k e   t h e   k e y   f o r   o b j e c t s   s t o r e d   i n   a n d   r e t r i e v e d   f r o m   i t e m s ,   a n d  
         / /   s h o u l d   b e   d e t e r m i n i s t i c .  
         k e y F u n c   K e y F u n c  
 }  
  
 t y p e   S t o r e   i n t e r f a c e   {  
         A d d ( o b j   i n t e r f a c e { } )   e r r o r  
         U p d a t e ( o b j   i n t e r f a c e { } )   e r r o r  
         D e l e t e ( o b j   i n t e r f a c e { } )   e r r o r  
         L i s t ( )   [ ] i n t e r f a c e { }  
         L i s t K e y s ( )   [ ] s t r i n g  
         G e t ( o b j   i n t e r f a c e { } )   ( i t e m   i n t e r f a c e { } ,   e x i s t s   b o o l ,   e r r   e r r o r )  
         G e t B y K e y ( k e y   s t r i n g )   ( i t e m   i n t e r f a c e { } ,   e x i s t s   b o o l ,   e r r   e r r o r )  
  
         / /   R e p l a c e   w i l l   d e l e t e   t h e   c o n t e n t s   o f   t h e   s t o r e ,   u s i n g   i n s t e a d   t h e  
         / /   g i v e n   l i s t .   S t o r e   t a k e s   o w n e r s h i p   o f   t h e   l i s t ,   y o u   s h o u l d   n o t   r e f e r e n c e  
         / /   i t   a f t e r   c a l l i n g   t h i s   f u n c t i o n .  
         R e p l a c e ( [ ] i n t e r f a c e { } ,   s t r i n g )   e r r o r  
         R e s y n c ( )   e r r o r  
 } Y6R�Nx 
 ` ` `  
  
 # #   f a c a d e   /   a d a p t e r   /   d e c o r a t o r   /   d e l e g a t e   /   b r i d g e   /   m e d i a t o r   /   c o m p o s i t e  
  
 �~T!j_�vNTb__�ُ�N��Y�S���_NN(u�mvzvQ-N�v:S+R0 
  
 # #   s i n g l e t o n  
  
 k u b e r n e t e s / g o l a n g   (u�_�_\� N,�O(uhQ@\�Sϑ( �YM�n)   ( �k�Y  n e t / h t t p   p a c k a g e   �v  h t t p . D e f a u l t C l i e n t   �T  h t t p . D e f a u l t S e r v e M u x ) .     b�\O:Nc o n t e x t  O�0 
 �[�s�e_�S�N�S�[ m a r c i o . i o / 2 0 1 5 / 0 7 / s i n & ] ( h t t p : / / m a r c i o . i o / 2 0 1 5 / 0 7 / s i n g l e t o n - p a t t e r n - i n - g o / )  
  
 �k��8^���v N�y�e_/fd o u b l e   c h e c k  
  
 ` ` `  
 f u n c   G e t I n s t a n c e ( )   * s i n g l e t o n   {  
         i f   i n s t a n c e   = =   n i l   {           / /   < - -   N o t   y e t   p e r f e c t .   s i n c e   i t ' s   n o t   f u l l y   a t o m i c  
                 m u . L o c k ( )  
                 d e f e r   m u . U n l o c k ( )  
  
                 i f   i n s t a n c e   = =   n i l   {  
                         i n s t a n c e   =   & s i n g l e t o n { }  
                 }  
         }  
         r e t u r n   i n s t a n c e  
 } Y6R�Nx 
 ` ` `  
  
 FO/f(Wg o l a n g ̑b�	g�f}Y�v N�y�e_�(u" O n c e "  
  
 ` ` `  
 t y p e   s i n g l e t o n   s t r u c t   {  
 }  
  
 v a r   i n s t a n c e   * s i n g l e t o n  
 v a r   o n c e   s y n c . O n c e  
  
 f u n c   G e t I n s t a n c e ( )   * s i n g l e t o n   {  
         o n c e . D o ( f u n c ( )   {  
                 i n s t a n c e   =   & s i n g l e t o n { }  
         } )  
         r e t u r n   i n s t a n c e  
 } Y6R�Nx 
 ` ` `  
  
 # #   f a c t o r y /   a b s t r a c t   f a c t o r y   �  b u i l d e r  
  
 sQ�Nُ�Q�yc r e a t i o n a l   p a t t e r n s   �v:S+R:  
  
 -   B u i l d e r   f o c u s e s   o n   c o n s t r u c t i n g   a   c o m p l e x   o b j e c t   s t e p   b y   s t e p .   A b s t r a c t   F a c t o r y   e m p h a s i z e s   a   f a m i l y   o f   p r o d u c t   o b j e c t s   ( e i t h e r   s i m p l e   o r   c o m p l e x ) .   B u i l d e r   r e t u r n s   t h e   p r o d u c t   a s   a   f i n a l   s t e p ,   b u t   a s   f a r   a s   t h e   A b s t r a c t   F a c t o r y   i s   c o n c e r n e d ,   t h e   p r o d u c t   g e t s   r e t u r n e d   i m m e d i a t e l y .  
 -   B u i l d e r   o f t e n   b u i l d s   a   C o m p o s i t e .  
 -   O f t e n ,   d e s i g n s   s t a r t   o u t   u s i n g   F a c t o r y   M e t h o d   ( l e s s   c o m p l i c a t e d ,   m o r e   c u s t o m i z a b l e ,   s u b c l a s s e s   p r o l i f e r a t e )   a n d   e v o l v e   t o w a r d   A b s t r a c t   F a c t o r y ,   P r o t o t y p e ,   o r   B u i l d e r   ( m o r e   f l e x i b l e ,   m o r e   c o m p l e x )   a s   t h e   d e s i g n e r   d i s c o v e r s   w h e r e   m o r e   f l e x i b i l i t y   i s   n e e d e d .  
 -   S o m e t i m e s   c r e a t i o n a l   p a t t e r n s   a r e   c o m p l e m e n t a r y :   B u i l d e r   c a n   u s e   o n e   o f   t h e   o t h e r   p a t t e r n s   t o   i m p l e m e n t   w h i c h   c o m p o n e n t s   g e t   b u i l t .   A b s t r a c t   F a c t o r y ,   B u i l d e r ,   a n d   P r o t o t y p e   c a n   u s e   S i n g l e t o n   i n   t h e i r   i m p l e m e n t a t i o n s .  
  
 f a c t o r y  
  
 ` ` `  
 / /   k 8 s . i o / k u b e r n e t e s / v e n d o r / k 8 s . i o / a p i m a c h i n e r y / p k g / r u n t i m e / s e r i a l i z e r / c o d e c _ f a c t o r y . g o  
 f u n c   N e w C o d e c F a c t o r y ( s c h e m e   * r u n t i m e . S c h e m e )   C o d e c F a c t o r y   {  
         s e r i a l i z e r s   : =   n e w S e r i a l i z e r s F o r S c h e m e ( s c h e m e ,   j s o n . D e f a u l t M e t a F a c t o r y )  
         r e t u r n   n e w C o d e c F a c t o r y ( s c h e m e ,   s e r i a l i z e r s )  
 }  
  
 f u n c   ( f   C o d e c F a c t o r y )   L e g a c y C o d e c ( v e r s i o n   . . . s c h e m a . G r o u p V e r s i o n )   r u n t i m e . C o d e c   {  
         r e t u r n   v e r s i o n i n g . N e w D e f a u l t i n g C o d e c F o r S c h e m e ( f . s c h e m e ,   f . l e g a c y S e r i a l i z e r ,   f . u n i v e r s a l ,   s c h e m a . G r o u p V e r s i o n s ( v e r s i o n ) ,   r u n t i m e . I n t e r n a l G r o u p V e r s i o n e r )  
 } Y6R�Nx 
 ` ` `  
  
 a b s t r a c t   f a c t o r y   �NS h a r e d I n f o r m e r F a c t o r y :N�O�ُ*Nf a c t o r y   ��Yc r e a t e   a p p / c o r e / b a t c h   . . . I{T�yi n t e r f a c e  
  
 ` ` `  
 / / k 8 s . i o / k u b e r n e t e s / p k g / c l i e n t / i n f o r m e r s / i n f o r m e r s _ g e n e r a t e d / i n t e r n a l v e r s i o n / f a c t o r y . g o  
 f u n c   N e w S h a r e d I n f o r m e r F a c t o r y ( c l i e n t   i n t e r n a l c l i e n t s e t . I n t e r f a c e ,   d e f a u l t R e s y n c   t i m e . D u r a t i o n )   S h a r e d I n f o r m e r F a c t o r y   {  
         r e t u r n   & s h a r e d I n f o r m e r F a c t o r y {  
                 c l i e n t :                       c l i e n t ,  
                 d e f a u l t R e s y n c :         d e f a u l t R e s y n c ,  
                 i n f o r m e r s :                 m a k e ( m a p [ r e f l e c t . T y p e ] c a c h e . S h a r e d I n d e x I n f o r m e r ) ,  
                 s t a r t e d I n f o r m e r s :   m a k e ( m a p [ r e f l e c t . T y p e ] b o o l ) ,  
         }  
 }  
  
 / /   S h a r e d I n f o r m e r F a c t o r y   p r o v i d e s   s h a r e d   i n f o r m e r s   f o r   r e s o u r c e s   i n   a l l   k n o w n  
 / /   A P I   g r o u p   v e r s i o n s .  
 t y p e   S h a r e d I n f o r m e r F a c t o r y   i n t e r f a c e   {  
         i n t e r n a l i n t e r f a c e s . S h a r e d I n f o r m e r F a c t o r y  
         F o r R e s o u r c e ( r e s o u r c e   s c h e m a . G r o u p V e r s i o n R e s o u r c e )   ( G e n e r i c I n f o r m e r ,   e r r o r )  
         W a i t F o r C a c h e S y n c ( s t o p C h   < - c h a n   s t r u c t { } )   m a p [ r e f l e c t . T y p e ] b o o l  
  
         A d m i s s i o n r e g i s t r a t i o n ( )   a d m i s s i o n r e g i s t r a t i o n . I n t e r f a c e  
         A p p s ( )   a p p s . I n t e r f a c e  
         A u t o s c a l i n g ( )   a u t o s c a l i n g . I n t e r f a c e  
         B a t c h ( )   b a t c h . I n t e r f a c e  
         C e r t i f i c a t e s ( )   c e r t i f i c a t e s . I n t e r f a c e  
         C o r e ( )   c o r e . I n t e r f a c e  
         E x t e n s i o n s ( )   e x t e n s i o n s . I n t e r f a c e  
         N e t w o r k i n g ( )   n e t w o r k i n g . I n t e r f a c e  
         P o l i c y ( )   p o l i c y . I n t e r f a c e  
         R b a c ( )   r b a c . I n t e r f a c e  
         S c h e d u l i n g ( )   s c h e d u l i n g . I n t e r f a c e  
         S e t t i n g s ( )   s e t t i n g s . I n t e r f a c e  
         S t o r a g e ( )   s t o r a g e . I n t e r f a c e  
 }  
  
 / /   s h a r e d I n f o r m e r F a c t o r y   /fwQSO�vs t u c t  
 f u n c   ( f   * s h a r e d I n f o r m e r F a c t o r y )   A p p s ( )   a p p s . I n t e r f a c e   {  
         r e t u r n   a p p s . N e w ( f )  
 } Y6R�Nx 
 ` ` `  
  
 b u i l d e r    
  
 ` ` `  
 / /   k 8 s . i o / k u b e r n e t e s / p k g / c o n t r o l l e r / c l i e n t _ b u i l d e r . g o  
  
 f u n c   N e w F o r C o n f i g O r D i e ( c   * r e s t . C o n f i g )   * C l i e n t s e t   {  
         v a r   c s   C l i e n t s e t  
         c s . a d m i s s i o n r e g i s t r a t i o n V 1 a l p h a 1   =   a d m i s s i o n r e g i s t r a t i o n v 1 a l p h a 1 . N e w F o r C o n f i g O r D i e ( c )  
         c s . a p p s V 1 b e t a 1   =   a p p s v 1 b e t a 1 . N e w F o r C o n f i g O r D i e ( c )  
         c s . a p p s V 1 b e t a 2   =   a p p s v 1 b e t a 2 . N e w F o r C o n f i g O r D i e ( c )  
         c s . a p p s V 1   =   a p p s v 1 . N e w F o r C o n f i g O r D i e ( c )  
         c s . a u t h e n t i c a t i o n V 1   =   a u t h e n t i c a t i o n v 1 . N e w F o r C o n f i g O r D i e ( c )  
         c s . a u t h e n t i c a t i o n V 1 b e t a 1   =   a u t h e n t i c a t i o n v 1 b e t a 1 . N e w F o r C o n f i g O r D i e ( c )  
         c s . a u t h o r i z a t i o n V 1   =   a u t h o r i z a t i o n v 1 . N e w F o r C o n f i g O r D i e ( c )  
         c s . a u t h o r i z a t i o n V 1 b e t a 1   =   a u t h o r i z a t i o n v 1 b e t a 1 . N e w F o r C o n f i g O r D i e ( c )  
         c s . a u t o s c a l i n g V 1   =   a u t o s c a l i n g v 1 . N e w F o r C o n f i g O r D i e ( c )  
         c s . a u t o s c a l i n g V 2 b e t a 1   =   a u t o s c a l i n g v 2 b e t a 1 . N e w F o r C o n f i g O r D i e ( c )  
         c s . b a t c h V 1   =   b a t c h v 1 . N e w F o r C o n f i g O r D i e ( c )  
         c s . b a t c h V 1 b e t a 1   =   b a t c h v 1 b e t a 1 . N e w F o r C o n f i g O r D i e ( c )  
         c s . b a t c h V 2 a l p h a 1   =   b a t c h v 2 a l p h a 1 . N e w F o r C o n f i g O r D i e ( c )  
         c s . c e r t i f i c a t e s V 1 b e t a 1   =   c e r t i f i c a t e s v 1 b e t a 1 . N e w F o r C o n f i g O r D i e ( c )  
         c s . c o r e V 1   =   c o r e v 1 . N e w F o r C o n f i g O r D i e ( c )  
         c s . e x t e n s i o n s V 1 b e t a 1   =   e x t e n s i o n s v 1 b e t a 1 . N e w F o r C o n f i g O r D i e ( c )  
         c s . n e t w o r k i n g V 1   =   n e t w o r k i n g v 1 . N e w F o r C o n f i g O r D i e ( c )  
         c s . p o l i c y V 1 b e t a 1   =   p o l i c y v 1 b e t a 1 . N e w F o r C o n f i g O r D i e ( c )  
         c s . r b a c V 1   =   r b a c v 1 . N e w F o r C o n f i g O r D i e ( c )  
         c s . r b a c V 1 b e t a 1   =   r b a c v 1 b e t a 1 . N e w F o r C o n f i g O r D i e ( c )  
         c s . r b a c V 1 a l p h a 1   =   r b a c v 1 a l p h a 1 . N e w F o r C o n f i g O r D i e ( c )  
         c s . s c h e d u l i n g V 1 a l p h a 1   =   s c h e d u l i n g v 1 a l p h a 1 . N e w F o r C o n f i g O r D i e ( c )  
         c s . s e t t i n g s V 1 a l p h a 1   =   s e t t i n g s v 1 a l p h a 1 . N e w F o r C o n f i g O r D i e ( c )  
         c s . s t o r a g e V 1 b e t a 1   =   s t o r a g e v 1 b e t a 1 . N e w F o r C o n f i g O r D i e ( c )  
         c s . s t o r a g e V 1   =   s t o r a g e v 1 . N e w F o r C o n f i g O r D i e ( c )  
  
         c s . D i s c o v e r y C l i e n t   =   d i s c o v e r y . N e w D i s c o v e r y C l i e n t F o r C o n f i g O r D i e ( c )  
         r e t u r n   & c s  
 } Y6R�Nx 
 ` ` `  
  
 # #   p r o t o t y p e  
  
 �S�W!j_/fR�^�W!j_�v N�y�vQyr�p(W�N�Ǐ Y6R  N*N�]�~X[(W�v�[�Oegԏ�V�e�v�[�O, �N/f�e�^�[�O0��Y6R�v�[�O1\/fb�N@b�y�v �S�W �ُ*N�S�W/f�S�[6R�v0 
 T h e   P r o t o t y p e   P a t t e r n   c r e a t e s   d u p l i c a t e   o b j e c t s   w h i l e   k e e p i n g   ` p e r f o r m a n c e `   i n   m i n d .   I t ' s   a   p a r t   o f   t h e   c r e a t i o n a l   p a t t e r n s   a n d   p r o v i d e s   o n e   o f   t h e   b e s t   w a y s   t o   c r e a t e   a n   o b j e c t .  
  
 �S�[ b l o g . r a l c h . c o m / t u t o r i a l / d e & ] ( h t t p : / / b l o g . r a l c h . c o m / t u t o r i a l / d e s i g n - p a t t e r n s / g o l a n g - p r o t o t y p e / )  
  
 k u b e r n e t e s O(u�Nd e e p c o p y - g e n ꁨRub�[a��vd e e p c o p y I{�e�l��k�YNb��v N*Nub�v�OP[ 
  
 ` ` `  
 / /   k 8 s . i o / k u b e r n e t e s / v e n d o r / k 8 s . i o / a p i s e r v e r / p k g / a p i s / a u d i t / z z _ g e n e r a t e d . d e e p c o p y . g o  
 / /   D e e p C o p y I n t o   i s   a n   a u t o g e n e r a t e d   d e e p c o p y   f u n c t i o n ,   c o p y i n g   t h e   r e c e i v e r ,   w r i t i n g   i n t o   o u t .   i n   m u s t   b e   n o n - n i l .  
 f u n c   ( i n   * G r o u p R e s o u r c e s )   D e e p C o p y I n t o ( o u t   * G r o u p R e s o u r c e s )   {  
         * o u t   =   * i n  
         i f   i n . R e s o u r c e s   ! =   n i l   {  
                 i n ,   o u t   : =   & i n . R e s o u r c e s ,   & o u t . R e s o u r c e s  
                 * o u t   =   m a k e ( [ ] s t r i n g ,   l e n ( * i n ) )  
                 c o p y ( * o u t ,   * i n )  
         }  
         i f   i n . R e s o u r c e N a m e s   ! =   n i l   {  
                 i n ,   o u t   : =   & i n . R e s o u r c e N a m e s ,   & o u t . R e s o u r c e N a m e s  
                 * o u t   =   m a k e ( [ ] s t r i n g ,   l e n ( * i n ) )  
                 c o p y ( * o u t ,   * i n )  
         }  
         r e t u r n  
 }  
  
 / /   D e e p C o p y   i s   a n   a u t o g e n e r a t e d   d e e p c o p y   f u n c t i o n ,   c o p y i n g   t h e   r e c e i v e r ,   c r e a t i n g   a   n e w   G r o u p R e s o u r c e s .  
 f u n c   ( i n   * G r o u p R e s o u r c e s )   D e e p C o p y ( )   * G r o u p R e s o u r c e s   {  
         i f   i n   = =   n i l   {  
                 r e t u r n   n i l  
         }  
         o u t   : =   n e w ( G r o u p R e s o u r c e s )  
         i n . D e e p C o p y I n t o ( o u t )  
         r e t u r n   o u t  
 } Y6R�Nx 
 ` ` `  
  
 ub�v�]wQ(Wُ̑  k 8 s . i o / k u b e r n e t e s / v e n d o r / k 8 s . i o / c o d e - g e n e r a t o r / c m d / d e e p c o p y - g e n / m a i n . g o  
 O(u  [ g i t h u b . c o m / k u b e r n e t e s / & ] ( h t t p s : / / g i t h u b . c o m / k u b e r n e t e s / g e n g o )  
  
 # #   o b s e r v e r  
  
 ُ*N!j_(Wk u b e r n e t e s ̑b�_N�k��8^����k�Ys h a r e d I n f o r m e r 1\/f N*N�[�!j_�v�[�s 
  
 ` ` `  
 / /   k 8 s . i o / c l i e n t - g o / t o o l s / c a c h e / s h a r e d _ i n f o r m e r . g o  
 f u n c   ( s   * s h a r e d I n d e x I n f o r m e r )   A d d E v e n t H a n d l e r W i t h R e s y n c P e r i o d ( h a n d l e r   R e s o u r c e E v e n t H a n d l e r ,   r e s y n c P e r i o d   t i m e . D u r a t i o n )   {  
         . . .  
         s . p r o c e s s o r . a d d L i s t e n e r ( l i s t e n e r )  
         . . .  
 }  
  
  
 / /   R�S 
 f u n c   ( p   * s h a r e d P r o c e s s o r )   d i s t r i b u t e ( o b j   i n t e r f a c e { } ,   s y n c   b o o l )   {  
         p . l i s t e n e r s L o c k . R L o c k ( )  
         d e f e r   p . l i s t e n e r s L o c k . R U n l o c k ( )  
  
         i f   s y n c   {  
                 f o r   _ ,   l i s t e n e r   : =   r a n g e   p . s y n c i n g L i s t e n e r s   {  
                         l i s t e n e r . a d d ( o b j )  
                 }  
         }   e l s e   {  
                 f o r   _ ,   l i s t e n e r   : =   r a n g e   p . l i s t e n e r s   {  
                         l i s t e n e r . a d d ( o b j )  
                 }  
         }  
 } Y6R�Nx 
 ` ` `  
  
 # #   c o m m a n d  
  
 �[IN:   }T�N!j_( C o m m a n d   P a t t e r n ) �\ N*N��Bl\ň:N N*N�[a���N�Ob�N�S(uNT�v��Bl�[�[7bۏL��SpeS��[��Bl�c�b���U_��Bl�e�_��N�S/ec�S�d ��v�d\O0}T�N!j_/f N�y�[a�L�:N�W!j_�vQ+RT:N�R\O( A c t i o n ) !j_b�N�R( T r a n s a c t i o n ) !j_0 
 k u b e r n e t e s   �vc o m m a n d   �W�N  g i t h u b . c o m / s p f 1 3 / c o b r a ,   �b}T�N�Sb�N�[a���k�Yc m d R o l l O u t ؏�[�s�Nu n d o 0 
  
 # #   i n t e r a t o r  
  
 �Tpenc�~�g�vsQ�vp a c k a g e ̑b�(u�_�k��Y. �Y_(u�v�^j s o n i t e r ,   b t r e e ,   g o v a l i d a t o r .  
  
 ` ` `  
 / /   g o l a n g h�Q�^  " g o / t o k e n "   �[�s�NI t e r a t e �e�l�FO/fvQ�[ُ̑�f�Pv i s t o r !j_. . .  
 f u n c   ( s   * F i l e S e t )   I t e r a t e ( f   f u n c ( * F i l e )   b o o l ) Y6R�Nx 
 ` ` `  
  
 # #   s t r a t e g y  
  
 �[IN N�|R�{�l���ُ�N�{�l(WЏL��e�S�N�Nbc�O�_R�y�{�l�&{T _핟SR0�[a�	g�g*NL�:N�FO/f(WNT�v:Wof-N��L�:N	gNT�v�[�s�{�l0 
 �[E�
NO(ui n t e r f a c e �v���P/fs t r a t e g y !j_��Nُ�eb�ws t r a t e g y !j_�S/fW[b�
N�v:_�aIN��[�s
N�Ti n t e r f a c e   �[�s�vf a c t o r y !j_�S/f:_��v�pN N7h� N*N/f:_�R�^�W� N*N/f:_�L�:N�W 
 �OP[ 
  
 ` ` `  
 / /   k 8 s �k�y�[a����[�^�N N*Ns t r a t e g y ��Q�[�Nu p d a t e , d e l e t e , g e t   �vV{eu 
 / /   �k�Y  / k 8 s . i o / k u b e r n e t e s / p k g / r e g i s t r y / c o r e / c o n f i g m a p / s t r a t e g y . g o  
  
 / /   s t r a t e g y   i m p l e m e n t s   b e h a v i o r   f o r   C o n f i g M a p   o b j e c t s  
 t y p e   s t r a t e g y   s t r u c t   {  
         r u n t i m e . O b j e c t T y p e r  
         n a m e s . N a m e G e n e r a t o r  
 }  
  
 / /   S t r a t e g y   i s   t h e   d e f a u l t   l o g i c   t h a t   a p p l i e s   w h e n   c r e a t i n g   a n d   u p d a t i n g   C o n f i g M a p  
 / /   o b j e c t s   v i a   t h e   R E S T   A P I .  
 v a r   S t r a t e g y   =   s t r a t e g y { a p i . S c h e m e ,   n a m e s . S i m p l e N a m e G e n e r a t o r }  
  
 / /   S t r a t e g y   s h o u l d   i m p l e m e n t   r e s t . R E S T C r e a t e S t r a t e g y  
 v a r   _   r e s t . R E S T C r e a t e S t r a t e g y   =   S t r a t e g y  
  
 / /   S t r a t e g y   s h o u l d   i m p l e m e n t   r e s t . R E S T U p d a t e S t r a t e g y  
 v a r   _   r e s t . R E S T U p d a t e S t r a t e g y   =   S t r a t e g y  
  
 f u n c   ( s t r a t e g y )   N a m e s p a c e S c o p e d ( )   b o o l   {  
         r e t u r n   t r u e  
 }  
  
 f u n c   ( s t r a t e g y )   P r e p a r e F o r C r e a t e ( c t x   g e n e r i c a p i r e q u e s t . C o n t e x t ,   o b j   r u n t i m e . O b j e c t )   {  
         _   =   o b j . ( * a p i . C o n f i g M a p )  
 }  
  
 f u n c   ( s t r a t e g y )   V a l i d a t e ( c t x   g e n e r i c a p i r e q u e s t . C o n t e x t ,   o b j   r u n t i m e . O b j e c t )   f i e l d . E r r o r L i s t   {  
         c f g   : =   o b j . ( * a p i . C o n f i g M a p )  
  
         r e t u r n   v a l i d a t i o n . V a l i d a t e C o n f i g M a p ( c f g )  
 }  
  
 / /   C a n o n i c a l i z e   n o r m a l i z e s   t h e   o b j e c t   a f t e r   v a l i d a t i o n .  
 f u n c   ( s t r a t e g y )   C a n o n i c a l i z e ( o b j   r u n t i m e . O b j e c t )   {  
 }  
  
 f u n c   ( s t r a t e g y )   A l l o w C r e a t e O n U p d a t e ( )   b o o l   {  
         r e t u r n   f a l s e  
 }  
  
 f u n c   ( s t r a t e g y )   P r e p a r e F o r U p d a t e ( c t x   g e n e r i c a p i r e q u e s t . C o n t e x t ,   n e w O b j ,   o l d O b j   r u n t i m e . O b j e c t )   {  
         _   =   o l d O b j . ( * a p i . C o n f i g M a p )  
         _   =   n e w O b j . ( * a p i . C o n f i g M a p )  
 }  
  
 f u n c   ( s t r a t e g y )   A l l o w U n c o n d i t i o n a l U p d a t e ( )   b o o l   {  
         r e t u r n   t r u e  
 }  
  
 f u n c   ( s t r a t e g y )   V a l i d a t e U p d a t e ( c t x   g e n e r i c a p i r e q u e s t . C o n t e x t ,   n e w O b j ,   o l d O b j   r u n t i m e . O b j e c t )   f i e l d . E r r o r L i s t   {  
         o l d C f g ,   n e w C f g   : =   o l d O b j . ( * a p i . C o n f i g M a p ) ,   n e w O b j . ( * a p i . C o n f i g M a p )  
  
         r e t u r n   v a l i d a t i o n . V a l i d a t e C o n f i g M a p U p d a t e ( n e w C f g ,   o l d C f g )  
 }  
  
  
  
 / /   k 8 s . i o / k u b e r n e t e s / p k g / r e g i s t r y / c o r e / c o n f i g m a p / s t o r a g e / s t o r a g e . g o  
 / /   N e w R E S T   r e t u r n s   a   R E S T S t o r a g e   o b j e c t   t h a t   w i l l   w o r k   w i t h   C o n f i g M a p   o b j e c t s .  
 f u n c   N e w R E S T ( o p t s G e t t e r   g e n e r i c . R E S T O p t i o n s G e t t e r )   * R E S T   {  
         s t o r e   : =   & g e n e r i c r e g i s t r y . S t o r e {  
                 N e w F u n c :                                     f u n c ( )   r u n t i m e . O b j e c t   {   r e t u r n   & a p i . C o n f i g M a p { }   } ,  
                 N e w L i s t F u n c :                             f u n c ( )   r u n t i m e . O b j e c t   {   r e t u r n   & a p i . C o n f i g M a p L i s t { }   } ,  
                 D e f a u l t Q u a l i f i e d R e s o u r c e :   a p i . R e s o u r c e ( " c o n f i g m a p s " ) ,  
  
                 C r e a t e S t r a t e g y :   c o n f i g m a p . S t r a t e g y ,  
                 U p d a t e S t r a t e g y :   c o n f i g m a p . S t r a t e g y ,  
                 D e l e t e S t r a t e g y :   c o n f i g m a p . S t r a t e g y ,  
         }  
         o p t i o n s   : =   & g e n e r i c . S t o r e O p t i o n s { R E S T O p t i o n s :   o p t s G e t t e r }  
         i f   e r r   : =   s t o r e . C o m p l e t e W i t h O p t i o n s ( o p t i o n s ) ;   e r r   ! =   n i l   {  
                 p a n i c ( e r r )   / /   T O D O :   P r o p a g a t e   e r r o r   u p  
         }  
         r e t u r n   & R E S T { s t o r e }  
 } Y6R�Nx 
 ` ` `  
  
 # #   s t a t e  
  
 �r`!j_( S t a t e   P a t t e r n )   �AQ�� N*N�[a�(WvQ�Q萶r`9e�S�e9e�S�[�vL�:N��[a�ww�eg<ONN�O9e�N�[�v{|0vQ+RT:N�r`�[a�( O b j e c t s   f o r   S t a t e s ) ��r`!j_/f N�y�[a�L�:N�W!j_0 
 R�y�r`�TL�:N��k�e� N*N�r`:g�v�[�s�1\/f N*Nh�Q�vs t a t e   !j_ 
  
 ` ` `  
 / /   k 8 s . i o / k u b e r n e t e s / v e n d o r / g i t h u b . c o m / c o r e o s / e t c d / r a f t / n o d e . g o  
 / /   N o d e   r e p r e s e n t s   a   n o d e   i n   a   r a f t   c l u s t e r .  
 t y p e   N o d e   i n t e r f a c e   {  
         . . . .  
         S t e p ( c t x   c o n t e x t . C o n t e x t ,   m s g   p b . M e s s a g e )   e r r o r  
  
         . . . .  
  
         / /   S t a t u s   r e t u r n s   t h e   c u r r e n t   s t a t u s   o f   t h e   r a f t   s t a t e   m a c h i n e .  
         S t a t u s ( )   S t a t u s  
         . . . .  
 } Y6R�Nx 
 ` ` `  
  
 # #   m e m e n t o  
  
 (WN4xOW\ň'`�vMR�cN�Uc�� N*N�[a��v�Q萶r`�v^(W��[a�KNY�OX[ُ*N�r`0ُ7h1\�S�N\��[a�b`Y0R�SHQ�OX[�v�r` 
  
 ` ` `  
 / /   k 8 s . i o / k u b e r n e t e s / p k g / r e g i s t r y / c o r e / s e r v i c e / p o r t a l l o c a t o r / a l l o c a t o r . g o  
 / /   N e w F r o m S n a p s h o t   a l l o c a t e s   a   P o r t A l l o c a t o r   a n d   i n i t i a l i z e s   i t   f r o m   a   s n a p s h o t .  
 f u n c   N e w F r o m S n a p s h o t ( s n a p   * a p i . R a n g e A l l o c a t i o n )   ( * P o r t A l l o c a t o r ,   e r r o r )   {  
         p r ,   e r r   : =   n e t . P a r s e P o r t R a n g e ( s n a p . R a n g e )  
         i f   e r r   ! =   n i l   {  
                 r e t u r n   n i l ,   e r r  
         }  
         r   : =   N e w P o r t A l l o c a t o r ( * p r )  
         i f   e r r   : =   r . R e s t o r e ( * p r ,   s n a p . D a t a ) ;   e r r   ! =   n i l   {  
                 r e t u r n   n i l ,   e r r  
         }  
         r e t u r n   r ,   n i l  
 }  
  
 f u n c   ( r   * P o r t A l l o c a t o r )   S n a p s h o t ( d s t   * a p i . R a n g e A l l o c a t i o n )   e r r o r   {  
         s n a p s h o t t a b l e ,   o k   : =   r . a l l o c . ( a l l o c a t o r . S n a p s h o t t a b l e )  
         i f   ! o k   {  
                 r e t u r n   f m t . E r r o r f ( " n o t   a   s n a p s h o t t a b l e   a l l o c a t o r " )  
         }  
         r a n g e S t r i n g ,   d a t a   : =   s n a p s h o t t a b l e . S n a p s h o t ( )  
         d s t . R a n g e   =   r a n g e S t r i n g  
         d s t . D a t a   =   d a t a  
         r e t u r n   n i l  
 } Y6R�Nx 
 ` ` `  
  
 ^IN
Nw�d e p l o y m e n t , s t a t e f u l s e t I{�[a��[�s�Nr o l l b a c k �e�l�_N/f{|<Om e m e t o ��k�Yd e p l o y m e n t 	gT�yv e r s i o n �vr e p l i c a s e t �vh i s t o r y Y�N�(u�Nb`Y�S�SHr,g0��~��k 8 s . i o / k u b e r n e t e s / p k g / c o n t r o l l e r / d e p l o y m e n t /  
  
 # #   f l y w e i g h t   /   o b j e c t   p o o l  
  
 f l y w e i g h t :_��v/f�[a�Y(u��To b j e c t   p o o l �v�v�v/f N7h�v0 
 O n e   d i f f e r e n c e   i n   t h a t   f l y w e i g h t s   a r e   c o m m o n l y   i m m u t a b l e   i n s t a n c e s ,   w h i l e   r e s o u r c e s   a c q u i r e d   f r o m   t h e   p o o l   u s u a l l y   a r e   m u t a b l e .  
 o b j e c t   p o o l (Wg o l a n g �Tk u b e r n e t e s (u�_�k��Y��k�Y�[�e1\	gs y n c . p o o l  
  
 ` ` `  
 / /   k 8 s . i o / k u b e r n e t e s / s t a g i n g / s r c / k 8 s . i o / a p i s e r v e r / p k g / s t o r a g e / c a c h e r . g o  
  
 v a r   t i m e r P o o l   s y n c . P o o l  
  
 f u n c   ( c   * c a c h e W a t c h e r )   a d d ( e v e n t   * w a t c h C a c h e E v e n t ,   b u d g e t   * t i m e B u d g e t )   {  
         . . .  
  
         t ,   o k   : =   t i m e r P o o l . G e t ( ) . ( * t i m e . T i m e r )  
         i f   o k   {  
                 t . R e s e t ( t i m e o u t )  
         }   e l s e   {  
                 t   =   t i m e . N e w T i m e r ( t i m e o u t )  
         }  
         d e f e r   t i m e r P o o l . P u t ( t )  
  
         . . . .  
 } Y6R�Nx 
 ` ` `  
  
 # #   i t e r p r e t e r  
  
 �ʑhV!j_�[IN NWY� ��e�l�v^������ ��ʑhV�O(u7b��O(uyr�[�e�l�c6R�ʑhVL�:N0 
 ُ*N(Wk u b e r n e t e s �vT�y�Nx��echub�]wQ-N(u�_�_Y0 
  
 # #   c h a i n _ o f _ r e s p o n s i b i l i t y  
  
 _N/f N�y�~T!j_. (u�v0W�e�_Y0L�#���!j_(u�NR�yNTL�#��v^N�R`�~T�vsQL�#�0���[a�S+TS_MRL�#��[a��N�SN N*NL�#���0 
  
 ` ` `  
 / /   ُ�yw r a p p e r   �b�QpeYt�N�~c h i l d r e n s  
 / /   k 8 s . i o / t e s t - i n f r a / v e l o d r o m e / t r a n s f o r m / p l u g i n s / m u l t i p l e x e r _ w r a p p e r . g o  
 f u n c   N e w M u l t i p l e x e r P l u g i n W r a p p e r ( p l u g i n s   . . . P l u g i n )   * M u l t i p l e x e r P l u g i n W r a p p e r   {  
         r e t u r n   & M u l t i p l e x e r P l u g i n W r a p p e r {  
                 p l u g i n s :   p l u g i n s ,  
         }  
 }  
  
 / /   ُ�yw a r p p e r   ��]Yt�[�N�NT�Q�N�~c l i l d r e n s  
 / /   k 8 s . i o / t e s t - i n f r a / v e l o d r o m e / t r a n s f o r m / p l u g i n s / a u t h o r _ l o g g e r _ w r a p p e r . g o  
 f u n c   N e w A u t h o r L o g g e r P l u g i n W r a p p e r ( p l u g i n   P l u g i n )   * A u t h o r L o g g e r P l u g i n W r a p p e r   {  
         r e t u r n   & A u t h o r L o g g e r P l u g i n W r a p p e r {  
                 p l u g i n :   p l u g i n ,  
         }  
 }  
  
 / /   ��]NYt��N�~c l i l d r e n s  
 . . . Y6R�Nx 
 ` ` `  
  
 # #   v i s i t  
  
 �[a��S����Yu�����c�S( �YA c c e p t ) RTg:N�[a��m�R�R���v�eP1\N ���9e�R�[a�0,g(�1\/f��Y��S�N�[IN N�yv i s i t ��]�[a��v�e�l��Nُ*N҉�^w��S��v i s i t \O:N N*N�Qpe O�1\/f N*Nv i s i t !j_0sS 
  
 ` ` `  
 f u n c ( a   * A ) V i s i t ( V i s t o r   f u n c ( * A )   e r r o r ) {  
         V i s t o r ( a )  
 } Y6R�Nx 
 ` ` `  
  
 �OP[ 
  
 ` ` `  
 / /   k 8 s . i o / k u b e r n e t e s / p k g / k u b e c t l / c m d / u t i l / o p e n a p i / o p e n a p i . g o  
 t y p e   S c h e m a V i s i t o r   i n t e r f a c e   {  
         V i s i t A r r a y ( * A r r a y )  
         V i s i t M a p ( * M a p )  
         V i s i t P r i m i t i v e ( * P r i m i t i v e )  
         V i s i t K i n d ( * K i n d )  
         V i s i t R e f e r e n c e ( R e f e r e n c e )  
 }  
  
 / /   S c h e m a   i s   t h e   b a s e   d e f i n i t i o n   o f   a n   o p e n a p i   t y p e .  
 t y p e   S c h e m a   i n t e r f a c e   {  
         / /   G i v i n g   a   v i s i t o r   h e r e   w i l l   l e t   y o u   v i s i t   t h e   a c t u a l   t y p e .  
         A c c e p t ( S c h e m a V i s i t o r )  
  
         / /   P r e t t y   p r i n t   t h e   n a m e   o f   t h e   t y p e .  
         G e t N a m e ( )   s t r i n g  
         / /   D e s c r i b e s   h o w   t o   a c c e s s   t h i s   f i e l d .  
         G e t P a t h ( )   * P a t h  
         / /   D e s c r i b e s   t h e   f i e l d .  
         G e t D e s c r i p t i o n ( )   s t r i n g  
         / /   R e t u r n s   t y p e   e x t e n s i o n s .  
         G e t E x t e n s i o n s ( )   m a p [ s t r i n g ] i n t e r f a c e { }  
 } Y6R�Nx 
 / /   / k 8 s . i o / k u b e r n e t e s / p k g / k u b e c t l / r e s o u r c e / b u i l d e r . g o  
 f u n c   ( b   * B u i l d e r )   v i s i t B y N a m e ( )   * R e s u l t   {  
         . . .  
  
         v i s i t o r s   : =   [ ] V i s i t o r { }  
         f o r   _ ,   n a m e   : =   r a n g e   b . n a m e s   {  
                 i n f o   : =   N e w I n f o ( c l i e n t ,   m a p p i n g ,   s e l e c t o r N a m e s p a c e ,   n a m e ,   b . e x p o r t )  
                 v i s i t o r s   =   a p p e n d ( v i s i t o r s ,   i n f o )  
         }  
         r e s u l t . v i s i t o r   =   V i s i t o r L i s t ( v i s i t o r s )  
         r e s u l t . s o u r c e s   =   v i s i t o r s  
         r e t u r n   r e s u l t  
 } Y6R�Nx 
 ` ` `  
  
 #   e n g i n e e r i n g     p a t t e r n s  
  
 