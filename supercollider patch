/*

Los pájaros en mí (fraccionamiento).
Estudio ornitológico de la escucha,
Síntesis basada en imitación.
Paisaje sonoro imaginario sintético.

Salamanca, Guanajuato.
6-13 de Abril del 2020.

*/

// 1. Open sky
(
~opensky={Limiter.ar(SinOsc.ar(Line.kr(4000,3900,5)+SinOsc.ar(7,0,100000),0,Pulse.kr(200,0.5,Line.kr(1,0,10))),0.8 )!2};

// 2. Ave de paso

~avedepaso={SinOsc.ar(Line.kr(4000,2,3)+SinOsc.ar(Line.kr(100000,10,0.5),0,10000),0,Pulse.kr(200,0.5,0.8))*EnvGen.kr(Env.perc(0.01,10,1),doneAction:2)!2};

// 3. Electroacoustic chirps

~electroacoustikChirps={SinOsc.ar(4000+SinOsc.ar(7,0,100000),0,Pulse.kr(EnvGen.kr(Env.new([5,3,1,0,20,200],[2,2,2,3,3,23]),doneAction:1),Line.kr(0.1,0.3,10),1))!2};

~electroacusticTone={SinOsc.ar(4000,0,Pulse.kr(EnvGen.kr(Env.new([5,3,1,0,20],[2,10,2,1,23]),doneAction:2),Line.kr(0.1,0.4,10),0.5))!2};

//Una transición para campo abierto.

~chowning={SinOsc.ar(11+SinOsc.ar(100021+SinOsc.ar(27,0,XLine.kr(123456,123456789,2.5)),0,12637),0,0.3)*EnvGen.kr(Env.perc(0.01,25,1))!2};

//campo abierto

~campoabierto={HPF.ar(SinOsc.ar(3+SinOsc.ar(20000+SinOsc.ar(10,0,10000),0,XLine.kr(100,1000,7)),0,LFTri.kr(EnvGen.kr(Env.new([2,11,7],[5,5,4]),doneAction:2),0,10)),1300)!2};

//ruidos paneados aleatorios

~noisepan={PanAz.ar(
	numChans:2,
	in: LPF.ar(ClipNoise.ar(1),Line.kr(20000,20000,10,doneAction:2)),
	pos:TRand.kr(-1,1,Impulse.kr(7)),
	level:1,
	width:0.2,
	orientation:0.3
)};

~noisepan2={PanAz.ar(
	numChans:4,
	in: LPF.ar(ClipNoise.ar(1),Line.kr(20000,20000,10,doneAction:2)),
	pos:TRand.kr(-1,1,Impulse.kr(7)),
	level:1,
	width:0.2,
	orientation:0.3
)};

// 7 de abril 2020

~chirps={SinOscFB.ar(8+SinOsc.ar(XLine.kr(16,4,0.3),0,20000),Line.kr(1,0,1),0.3)*EnvGen.kr(Env.new([1,1,1,0],[1,1,2,3]),doneAction:2)!2};

~cagadero={SinOscFB.ar(2+SinOsc.ar(1928+SinOsc.ar(7+SinOsc.ar(1,0,10),0,80),0,20000),0,0.4)*EnvGen.kr(Env.new([1,1,1,1],[1,1,2,3]),doneAction:2)!2};

~fm={LPF.ar(SinOsc.ar(10+SinOsc.ar(12345,0,[12345,12345].choose),0,0.1),8000,2)*EnvGen.ar(Env.adsr(0.5,3,0,0.5),doneAction:2)!2};

~pulse2000={SinOsc.ar(2000,0,Pulse.kr(8,0.17,1))*EnvGen.kr(Env.new([1,1,1],[1,1,]),doneAction:2)!2};

~takataka1={Pan2.ar(Impulse.ar(4,0,6)*ClipNoise.ar(2)*EnvGen.kr(Env.new([1,2],[3,2]),doneAction:2),-1)};

~takataka3={Pan2.ar(Impulse.ar(3,0,6)*ClipNoise.ar(2)*EnvGen.kr(Env.new([1,2],[2,2]),doneAction:2),1)};

~takataka2={Pan2.ar(Impulse.ar(10,0,6)*ClipNoise.ar(1)*EnvGen.kr(Env.new([1,2],[2,2]),doneAction:2),0)};

~takataka4={Pan2.ar(Impulse.ar(12,0,6)*ClipNoise.ar(1)*EnvGen.kr(Env.new([1,2],[2,2]),doneAction:2),0)};


//pajaros individuales

//10 de Abril 2020

~indbird1={SinOsc.ar(Line.kr(40000,2,4)+SinOsc.ar(Line.kr(400000,[20].choose,0.5),0,10000),0,Pulse.kr(200,0.5,1))*EnvGen.kr(Env.perc(0.01,6,1),doneAction:2)!2};

~indbird2={SinOsc.ar(Line.kr(40000,2,3)+SinOsc.ar(Line.kr(400000,[8,5,20].choose,0.5),0,10000),0,Pulse.kr(200,0.5,1))*EnvGen.kr(Env.perc(0.01,6,1),doneAction:2)!2};

~indbird3={SinOsc.ar(12+LFTri.ar(4+LFTri.ar(11.4+SinOsc.ar(12345,0,956),0,18909),0,25),0,0.5)*EnvGen.kr(Env.new([0.5,1],[2,2]),doneAction:2)!2};

~indbird4={HPF.ar(SinOsc.ar(12+LFTri.ar([45,4].choose+LFTri.ar([11.4,1]+SinOsc.ar(1234,0,956),0,18909),0,25),0,0.3)*EnvGen.kr(Env.new([1,2],[2,2]),doneAction:2),40)!2};

~indchirp1={HPF.ar(SinOsc.ar(12+LFTri.ar(4+LFTri.ar(110+SinOsc.ar(1023,0,956),0,18909),0,100),0,0.6)*EnvGen.kr(Env.new([1,2],[20,20]),doneAction:2),40)!2};

~indchirp2={HPF.ar(SinOsc.ar(12+LFTri.ar(4+LFTri.ar([1,10]+SinOsc.ar(1,0,[956,9561]),0,18909),0,100),0,0.5)*EnvGen.kr(Env.new([1,2],[10,10]),doneAction:2),40)!2};

~indchirp3={HPF.ar(SinOsc.ar(12+LFTri.ar(4+SinOsc.ar([1400,10]+SinOsc.ar([1,11],0.5,[9563,956]),0.5,18910),0,100),0,0.3)*EnvGen.kr(Env.new([2,2],[1.5,10]),doneAction:2),20)!2};

~indchirp4={HPF.ar(SinOsc.ar(12+LFTri.ar(4+SinOsc.ar([1400,10]+SinOsc.ar([1,10],0.5,[9563,956]),0.5,18910),0,100),0,0.3)*EnvGen.kr(Env.new([2,2],[1.5,10]),doneAction:2),20)!2};

~indchirp5={HPF.ar(SinOsc.ar(12+LFTri.ar(4+LFTri.ar(110+SinOsc.ar(103,0,11),0,18909),0,100),0,0.2)*EnvGen.kr(Env.new([1,2],[0.75,0]),doneAction:2),40)!2};

~whitenoise={WhiteNoise.ar(0.9)*EnvGen.kr(Env.new([1,1],[0.3,0.4]),doneAction:2)!2};
~whitenoise2={WhiteNoise.ar(0.5)*EnvGen.kr(Env.new([1,1],[0.3,0.4]),doneAction:2)!2};

~sinebass={SinOsc.ar(40,0,0.8)*EnvGen.kr(Env.new([1,1],[0.6,0]),doneAction:2)!2};

~sinebass2={SinOsc.ar(40,0,1)*EnvGen.kr(Env.perc(0,15,1),doneAction:2)!2};

// Bonus tracks - En caso de que salga algo que pueda dotar de mayor extension la pieza.
// 13 de Abril del 2020

~pajaro1={Pan2.ar(SinOsc.ar(10000+SinOsc.ar(Line.kr(3,2,0.1)+SinOsc.ar(4,0,7),0,Line.kr(172684,1726,1)),0,1)*EnvGen.kr(Env.new([1,1],[1.85,2]),doneAction:2),SinOsc.kr(0.5))};

~parvada1={HPF.ar(Pan2.ar(SinOsc.ar(90+SinOsc.ar(Line.kr(10,3,5)+SinOsc.ar(Line.kr(25600,7,2),0,Line.kr(1982,198200000,3)),1,10210),0,1)*EnvGen.kr(Env.new([1,1,0],[2,5,1]),doneAction:2),SinOsc.kr(0.1)),20)};

~parvada2={HPF.ar(Pan2.ar(SinOsc.ar(90+SinOsc.ar(Line.kr(10,3,5)+SinOsc.ar(Line.kr(256000,4,2),0,Line.kr(19820,19820000,3)),1,10210),0,1)*EnvGen.kr(Env.new([1,1,0.7],[2,4,1]),doneAction:2),SinOsc.kr(0.1)),20)};
)

// Rutina de aves individuales.
// 11 de Abril 2020

(
~lospajarosenmi=(
Routine{
	~fm.play;
	~indbird3.play;
	~chirps.play;
	2.wait;
	~indchirp5.play;
	~indbird1.play;
	~takataka2.play;
	2.wait;
	~sinebass.play;
	~indbird1.play;
	~indchirp4.play;
	~takataka2.play;
	2.wait;
	~whitenoise.play;
	~indbird1.play;
	2.wait;
	~indbird2.play;
	~pajaro1.play;
	2.wait;
	~whitenoise.play;
	~indbird2.play;
	2.wait;
	~indbird2.play;
	~takataka3.play;
	2.5.wait;
	~indchirp1.play;
	1.wait;
	~indchirp1.play;
	1.5.wait;
	~indchirp1.play;
	~takataka2.play;
	1.wait;
	~indchirp1.play;
	1.5.wait;
	~whitenoise.play;
	~takataka2.play;
	1.wait;
	~whitenoise.play;
	1.5.wait;
	~indchirp1.play;
	~indchirp2.play;
	~takataka1.play;
	1.wait;
	~indchirp1.play;
	~indchirp2.play;
	~takataka3.play;
	1.5.wait;
	~sinebass.play;
	~indchirp2.play;
	1.wait;
	~sinebass.play;
	~indchirp2.play;
	~takataka4.play;
	1.5.wait;
	~sinebass2.play;
	~opensky.play;
	5.wait;
	~avedepaso.play;
	2.wait;
	~avedepaso.play;
	1.95.wait;
	~electroacoustikChirps.play;
	5.wait;
	~chowning.play;
	2.wait;
	~chowning.play;
	3.wait;
	~campoabierto.play;
	2.wait;
	~campoabierto.play;
	0.5.wait;
	~campoabierto.play;
	~campoabierto.play;
	2.wait;
	~parvada1.play;
	~noisepan.play;
	~fm.play;
	2.wait;
	~indchirp3.play;
	2.wait;
	~indchirp3.play;
	~takataka4.play;
	2.wait;
	~noisepan2.play;
	~indchirp4.play;
	2.wait;
	~indchirp4.play;
	1.wait;
	~indchirp5.play;
	~takataka2.play;
	1.wait;
	~indbird4.play;
	1.wait;
	~cagadero.play;
	~parvada2.play;
	1.wait;
	~whitenoise.play;
	~indbird3.play;
	1.wait;
	~indbird4.play;
	~indchirp5.play;
	1.wait;
	~takataka2.play;
	1.wait;
	~takataka2.play;
	~fm.play;
	1.wait;
	~fm.play;
	~indchirp1.play;
	1.wait;
	~indchirp1.play;
	1.5.wait;
	~indchirp1.play;
	~takataka2.play;
	1.wait;
	~indchirp1.play;
	1.5.wait;
	~indchirp3.play;
	~indchirp1.play;
	1.wait;
	~indchirp1.play;
	1.5.wait;
	~indchirp1.play;
	1.wait;
    ~indchirp1.play;
	1.5.wait;
	~indchirp1.play;
	~pajaro1.play;
	1.wait;
	~sinebass.play;
	~indchirp1.play;
	~whitenoise2.play;
	0.1.wait;
	~indchirp5.play;
	1.5.wait;
	~sinebass.play;
	~whitenoise.play;
	1.wait;
	~sinebass.play;
	~whitenoise2.play;
	0.1.wait;
	~indchirp5.play;

});
)

~lospajarosenmi.play;

s.meter;
s.makeWindow;
s.plotTree;
s.freeAll;
