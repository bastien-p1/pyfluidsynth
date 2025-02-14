<html><head><title>Python: module fluidsynth</title>
</head><body bgcolor="#f0f0f8">

<table width="100%" cellspacing=0 cellpadding=2 border=0 summary="heading">
<tr bgcolor="#7799ee">
<td valign=bottom>&nbsp;<br>
<font color="#ffffff" face="helvetica, arial">&nbsp;<br><big><big><strong>fluidsynth</strong></big></big></font></td
><td align=right valign=bottom
><font color="#ffffff" face="helvetica, arial"><a href=".">index</a><br><a href="file:/home/nwhitehe/Projects/pygalaxy/pyfluidsynth/fluidsynth.py">/home/nwhitehe/Projects/pygalaxy/pyfluidsynth/fluidsynth.py</a></font></td></tr></table>
    <p><tt>pyFluidSynth<br>
&nbsp;<br>
Python&nbsp;bindings&nbsp;for&nbsp;FluidSynth<br>
&nbsp;<br>
Copyright&nbsp;2008,&nbsp;Nathan&nbsp;Whitehead&nbsp;&lt;nwhitehe@gmail.com&gt;<br>
Released&nbsp;under&nbsp;the&nbsp;LGPL<br>
&nbsp;<br>
This&nbsp;module&nbsp;contains&nbsp;python&nbsp;bindings&nbsp;for&nbsp;FluidSynth.&nbsp;&nbsp;FluidSynth&nbsp;is&nbsp;a<br>
software&nbsp;synthesizer&nbsp;for&nbsp;generating&nbsp;music.&nbsp;&nbsp;It&nbsp;works&nbsp;like&nbsp;a&nbsp;MIDI<br>
synthesizer.&nbsp;&nbsp;You&nbsp;load&nbsp;patches,&nbsp;set&nbsp;parameters,&nbsp;then&nbsp;send&nbsp;NOTEON&nbsp;and<br>
NOTEOFF&nbsp;events&nbsp;to&nbsp;play&nbsp;notes.&nbsp;&nbsp;Instruments&nbsp;are&nbsp;defined&nbsp;in&nbsp;SoundFonts,<br>
generally&nbsp;files&nbsp;with&nbsp;the&nbsp;extension&nbsp;SF2.&nbsp;&nbsp;FluidSynth&nbsp;can&nbsp;either&nbsp;be&nbsp;used<br>
to&nbsp;play&nbsp;audio&nbsp;itself,&nbsp;or&nbsp;you&nbsp;can&nbsp;call&nbsp;a&nbsp;function&nbsp;that&nbsp;returns&nbsp;chunks<br>
of&nbsp;audio&nbsp;data&nbsp;and&nbsp;output&nbsp;the&nbsp;data&nbsp;to&nbsp;the&nbsp;soundcard&nbsp;yourself.<br>
FluidSynth&nbsp;works&nbsp;on&nbsp;all&nbsp;major&nbsp;platforms,&nbsp;so&nbsp;pyFluidSynth&nbsp;should&nbsp;also.</tt></p>
<p>
<table width="100%" cellspacing=0 cellpadding=2 border=0 summary="section">
<tr bgcolor="#aa55cc">
<td colspan=3 valign=bottom>&nbsp;<br>
<font color="#fffff" face="helvetica, arial"><big><strong>Modules</strong></big></font></td></tr>
    
<tr><td bgcolor="#aa55cc"><tt>&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;</tt></td><td>&nbsp;</td>
<td width="100%"><table width="100%" summary="list"><tr><td width="25%" valign=top><a href="numpy.html">numpy</a><br>
</td><td width="25%" valign=top><a href="time.html">time</a><br>
</td><td width="25%" valign=top></td><td width="25%" valign=top></td></tr></table></td></tr></table><p>
<table width="100%" cellspacing=0 cellpadding=2 border=0 summary="section">
<tr bgcolor="#ee77aa">
<td colspan=3 valign=bottom>&nbsp;<br>
<font color="#ffffff" face="helvetica, arial"><big><strong>Classes</strong></big></font></td></tr>
    
<tr><td bgcolor="#ee77aa"><tt>&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;</tt></td><td>&nbsp;</td>
<td width="100%"><dl>
<dt><font face="helvetica, arial"><a href="fluidsynth.html#Synth">Synth</a>
</font></dt></dl>
 <p>
<table width="100%" cellspacing=0 cellpadding=2 border=0 summary="section">
<tr bgcolor="#ffc8d8">
<td colspan=3 valign=bottom>&nbsp;<br>
<font color="#000000" face="helvetica, arial"><a name="Synth">class <strong>Synth</strong></a></font></td></tr>
    
<tr bgcolor="#ffc8d8"><td rowspan=2><tt>&nbsp;&nbsp;&nbsp;</tt></td>
<td colspan=2><tt><a href="#Synth">Synth</a>&nbsp;represents&nbsp;a&nbsp;FluidSynth&nbsp;synthesizer<br>&nbsp;</tt></td></tr>
<tr><td>&nbsp;</td>
<td width="100%">Methods defined here:<br>
<dl><dt><a name="Synth-__init__"><strong>__init__</strong></a>(self, gain<font color="#909090">=0.20000000000000001</font>, samplerate<font color="#909090">=44100</font>)</dt><dd><tt>Create&nbsp;new&nbsp;synthesizer&nbsp;object&nbsp;to&nbsp;control&nbsp;sound&nbsp;generation<br>
&nbsp;<br>
Optional&nbsp;keyword&nbsp;arguments:<br>
&nbsp;&nbsp;gain&nbsp;:&nbsp;scale&nbsp;factor&nbsp;for&nbsp;audio&nbsp;output,&nbsp;default&nbsp;is&nbsp;0.2<br>
&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;lower&nbsp;values&nbsp;are&nbsp;quieter,&nbsp;allow&nbsp;more&nbsp;simultaneous&nbsp;notes<br>
&nbsp;&nbsp;samplerate&nbsp;:&nbsp;output&nbsp;samplerate&nbsp;in&nbsp;Hz,&nbsp;default&nbsp;is&nbsp;44100&nbsp;Hz</tt></dd></dl>

<dl><dt><a name="Synth-bank_select"><strong>bank_select</strong></a>(self, chan, bank)</dt><dd><tt>Choose&nbsp;a&nbsp;bank</tt></dd></dl>

<dl><dt><a name="Synth-cc"><strong>cc</strong></a>(self, chan, ctrl, val)</dt><dd><tt>Send&nbsp;control&nbsp;change&nbsp;value<br>
&nbsp;<br>
The&nbsp;controls&nbsp;that&nbsp;are&nbsp;recognized&nbsp;are&nbsp;dependent&nbsp;on&nbsp;the<br>
SoundFont.&nbsp;&nbsp;Values&nbsp;are&nbsp;always&nbsp;0&nbsp;to&nbsp;127.&nbsp;&nbsp;Typical&nbsp;controls<br>
include:<br>
&nbsp;&nbsp;1&nbsp;:&nbsp;vibrato<br>
&nbsp;&nbsp;7&nbsp;:&nbsp;volume<br>
&nbsp;&nbsp;10&nbsp;:&nbsp;pan&nbsp;(left&nbsp;to&nbsp;right)<br>
&nbsp;&nbsp;11&nbsp;:&nbsp;expression&nbsp;(soft&nbsp;to&nbsp;loud)<br>
&nbsp;&nbsp;64&nbsp;:&nbsp;sustain<br>
&nbsp;&nbsp;91&nbsp;:&nbsp;reverb<br>
&nbsp;&nbsp;93&nbsp;:&nbsp;chorus</tt></dd></dl>

<dl><dt><a name="Synth-delete"><strong>delete</strong></a>(self)</dt></dl>

<dl><dt><a name="Synth-get_samples"><strong>get_samples</strong></a>(self, len<font color="#909090">=1024</font>)</dt><dd><tt>Generate&nbsp;audio&nbsp;samples<br>
&nbsp;<br>
The&nbsp;return&nbsp;value&nbsp;will&nbsp;be&nbsp;a&nbsp;NumPy&nbsp;array&nbsp;containing&nbsp;the&nbsp;given<br>
length&nbsp;of&nbsp;audio&nbsp;samples.&nbsp;&nbsp;If&nbsp;the&nbsp;synth&nbsp;is&nbsp;set&nbsp;to&nbsp;stereo&nbsp;output<br>
(the&nbsp;default)&nbsp;the&nbsp;array&nbsp;will&nbsp;be&nbsp;size&nbsp;2&nbsp;*&nbsp;len.</tt></dd></dl>

<dl><dt><a name="Synth-noteoff"><strong>noteoff</strong></a>(self, chan, key)</dt><dd><tt>Stop&nbsp;a&nbsp;note</tt></dd></dl>

<dl><dt><a name="Synth-noteon"><strong>noteon</strong></a>(self, chan, key, vel)</dt><dd><tt>Play&nbsp;a&nbsp;note</tt></dd></dl>

<dl><dt><a name="Synth-pitch_bend"><strong>pitch_bend</strong></a>(self, chan, val)</dt><dd><tt>Adjust&nbsp;pitch&nbsp;of&nbsp;a&nbsp;playing&nbsp;channel&nbsp;by&nbsp;small&nbsp;amounts<br>
&nbsp;<br>
A&nbsp;pitch&nbsp;bend&nbsp;value&nbsp;of&nbsp;0&nbsp;is&nbsp;no&nbsp;pitch&nbsp;change&nbsp;from&nbsp;default.<br>
A&nbsp;value&nbsp;of&nbsp;-2048&nbsp;is&nbsp;1&nbsp;semitone&nbsp;down.<br>
A&nbsp;value&nbsp;of&nbsp;2048&nbsp;is&nbsp;1&nbsp;semitone&nbsp;up.<br>
Maximum&nbsp;values&nbsp;are&nbsp;-8192&nbsp;to&nbsp;+8192&nbsp;(transposing&nbsp;by&nbsp;4&nbsp;semitones).</tt></dd></dl>

<dl><dt><a name="Synth-program_change"><strong>program_change</strong></a>(self, chan, prg)</dt><dd><tt>Change&nbsp;the&nbsp;program</tt></dd></dl>

<dl><dt><a name="Synth-program_reset"><strong>program_reset</strong></a>(self)</dt><dd><tt>Reset&nbsp;the&nbsp;programs&nbsp;on&nbsp;all&nbsp;channels</tt></dd></dl>

<dl><dt><a name="Synth-program_select"><strong>program_select</strong></a>(self, chan, sfid, bank, preset)</dt><dd><tt>Select&nbsp;a&nbsp;program</tt></dd></dl>

<dl><dt><a name="Synth-sfload"><strong>sfload</strong></a>(self, filename, update_midi_preset<font color="#909090">=0</font>)</dt><dd><tt>Load&nbsp;SoundFont&nbsp;and&nbsp;return&nbsp;its&nbsp;ID</tt></dd></dl>

<dl><dt><a name="Synth-sfont_select"><strong>sfont_select</strong></a>(self, chan, sfid)</dt><dd><tt>Choose&nbsp;a&nbsp;SoundFont</tt></dd></dl>

<dl><dt><a name="Synth-sfunload"><strong>sfunload</strong></a>(self, sfid, update_midi_preset<font color="#909090">=0</font>)</dt><dd><tt>Unload&nbsp;a&nbsp;SoundFont&nbsp;and&nbsp;free&nbsp;memory&nbsp;it&nbsp;used</tt></dd></dl>

<dl><dt><a name="Synth-start"><strong>start</strong></a>(self, driver<font color="#909090">=None</font>)</dt><dd><tt>Start&nbsp;audio&nbsp;output&nbsp;driver&nbsp;in&nbsp;separate&nbsp;background&nbsp;thread<br>
&nbsp;<br>
Call&nbsp;this&nbsp;function&nbsp;any&nbsp;time&nbsp;after&nbsp;creating&nbsp;the&nbsp;<a href="#Synth">Synth</a>&nbsp;object.<br>
If&nbsp;you&nbsp;don't&nbsp;call&nbsp;this&nbsp;function,&nbsp;use&nbsp;<a href="#Synth-get_samples">get_samples</a>()&nbsp;to&nbsp;generate<br>
samples.<br>
&nbsp;<br>
Optional&nbsp;keyword&nbsp;argument:<br>
&nbsp;&nbsp;driver&nbsp;:&nbsp;which&nbsp;audio&nbsp;driver&nbsp;to&nbsp;use&nbsp;for&nbsp;output<br>
&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;Possible&nbsp;choices:<br>
&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;'alsa',&nbsp;'oss',&nbsp;'jack',&nbsp;'portaudio'<br>
&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;'sndmgr',&nbsp;'coreaudio',&nbsp;'Direct&nbsp;Sound'<br>
&nbsp;<br>
Not&nbsp;all&nbsp;drivers&nbsp;will&nbsp;be&nbsp;available&nbsp;for&nbsp;every&nbsp;platform,&nbsp;it<br>
depends&nbsp;on&nbsp;which&nbsp;drivers&nbsp;were&nbsp;compiled&nbsp;into&nbsp;FluidSynth&nbsp;for<br>
your&nbsp;platform.</tt></dd></dl>

<dl><dt><a name="Synth-system_reset"><strong>system_reset</strong></a>(self)</dt><dd><tt>Stop&nbsp;all&nbsp;notes&nbsp;and&nbsp;reset&nbsp;all&nbsp;programs</tt></dd></dl>

</td></tr></table></td></tr></table><p>
<table width="100%" cellspacing=0 cellpadding=2 border=0 summary="section">
<tr bgcolor="#eeaa77">
<td colspan=3 valign=bottom>&nbsp;<br>
<font color="#ffffff" face="helvetica, arial"><big><strong>Functions</strong></big></font></td></tr>
    
<tr><td bgcolor="#eeaa77"><tt>&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;</tt></td><td>&nbsp;</td>
<td width="100%"><dl><dt><a name="-addressof"><strong>addressof</strong></a>(...)</dt><dd><tt><a href="#-addressof">addressof</a>(C&nbsp;instance)&nbsp;-&gt;&nbsp;integer<br>
Return&nbsp;the&nbsp;address&nbsp;of&nbsp;the&nbsp;C&nbsp;instance&nbsp;internal&nbsp;buffer</tt></dd></dl>
 <dl><dt><a name="-alignment"><strong>alignment</strong></a>(...)</dt><dd><tt><a href="#-alignment">alignment</a>(C&nbsp;type)&nbsp;-&gt;&nbsp;integer<br>
<a href="#-alignment">alignment</a>(C&nbsp;instance)&nbsp;-&gt;&nbsp;integer<br>
Return&nbsp;the&nbsp;alignment&nbsp;requirements&nbsp;of&nbsp;a&nbsp;C&nbsp;instance</tt></dd></dl>
 <dl><dt><a name="-byref"><strong>byref</strong></a>(...)</dt><dd><tt><a href="#-byref">byref</a>(C&nbsp;instance)&nbsp;-&gt;&nbsp;byref-object<br>
Return&nbsp;a&nbsp;pointer&nbsp;lookalike&nbsp;to&nbsp;a&nbsp;C&nbsp;instance,&nbsp;only&nbsp;usable<br>
as&nbsp;function&nbsp;argument</tt></dd></dl>
 <dl><dt><a name="-cfunc"><strong>cfunc</strong></a>(name, result, *args)</dt><dd><tt>build&nbsp;and&nbsp;apply&nbsp;a&nbsp;ctypes&nbsp;prototype&nbsp;complete&nbsp;with&nbsp;parameter&nbsp;flags</tt></dd></dl>
 <dl><dt><a name="-fluid_synth_write_s16_stereo"><strong>fluid_synth_write_s16_stereo</strong></a>(synth, len)</dt><dd><tt>Return&nbsp;generated&nbsp;samples&nbsp;in&nbsp;stereo&nbsp;16-bit&nbsp;format<br>
&nbsp;<br>
Return&nbsp;value&nbsp;is&nbsp;a&nbsp;Numpy&nbsp;array&nbsp;of&nbsp;samples.</tt></dd></dl>
 <dl><dt><a name="-raw_audio_string"><strong>raw_audio_string</strong></a>(data)</dt><dd><tt>Return&nbsp;a&nbsp;string&nbsp;of&nbsp;bytes&nbsp;to&nbsp;send&nbsp;to&nbsp;soundcard<br>
&nbsp;<br>
Input&nbsp;is&nbsp;a&nbsp;numpy&nbsp;array&nbsp;of&nbsp;samples.&nbsp;&nbsp;Default&nbsp;output&nbsp;format<br>
is&nbsp;16-bit&nbsp;signed&nbsp;(other&nbsp;formats&nbsp;not&nbsp;currently&nbsp;supported).</tt></dd></dl>
 <dl><dt><a name="-resize"><strong>resize</strong></a>(...)</dt><dd><tt>Resize&nbsp;the&nbsp;memory&nbsp;buffer&nbsp;of&nbsp;a&nbsp;ctypes&nbsp;instance</tt></dd></dl>
 <dl><dt><a name="-set_conversion_mode"><strong>set_conversion_mode</strong></a>(...)</dt><dd><tt><a href="#-set_conversion_mode">set_conversion_mode</a>(encoding,&nbsp;errors)&nbsp;-&gt;&nbsp;(previous-encoding,&nbsp;previous-errors)<br>
&nbsp;<br>
Set&nbsp;the&nbsp;encoding&nbsp;and&nbsp;error&nbsp;handling&nbsp;ctypes&nbsp;uses&nbsp;when&nbsp;converting<br>
between&nbsp;unicode&nbsp;and&nbsp;strings.&nbsp;&nbsp;Returns&nbsp;the&nbsp;previous&nbsp;values.</tt></dd></dl>
 <dl><dt><a name="-sizeof"><strong>sizeof</strong></a>(...)</dt><dd><tt><a href="#-sizeof">sizeof</a>(C&nbsp;type)&nbsp;-&gt;&nbsp;integer<br>
<a href="#-sizeof">sizeof</a>(C&nbsp;instance)&nbsp;-&gt;&nbsp;integer<br>
Return&nbsp;the&nbsp;size&nbsp;in&nbsp;bytes&nbsp;of&nbsp;a&nbsp;C&nbsp;instance</tt></dd></dl>
</td></tr></table><p>
<table width="100%" cellspacing=0 cellpadding=2 border=0 summary="section">
<tr bgcolor="#55aa55">
<td colspan=3 valign=bottom>&nbsp;<br>
<font color="#ffffff" face="helvetica, arial"><big><strong>Data</strong></big></font></td></tr>
    
<tr><td bgcolor="#55aa55"><tt>&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;</tt></td><td>&nbsp;</td>
<td width="100%"><strong>DEFAULT_MODE</strong> = 0<br>
<strong>RTLD_GLOBAL</strong> = 256<br>
<strong>RTLD_LOCAL</strong> = 0<br>
<strong>api_version</strong> = '1.2'<br>
<strong>cdll</strong> = &lt;ctypes.LibraryLoader object at 0xb70758ec&gt;<br>
<strong>delete_fluid_audio_driver</strong> = &lt;CFunctionType object at 0xb7083304&gt;<br>
<strong>delete_fluid_settings</strong> = &lt;CFunctionType object at 0xb70833d4&gt;<br>
<strong>delete_fluid_synth</strong> = &lt;CFunctionType object at 0xb708336c&gt;<br>
<strong>fluid_settings_setint</strong> = &lt;CFunctionType object at 0xb708329c&gt;<br>
<strong>fluid_settings_setnum</strong> = &lt;CFunctionType object at 0xb7083234&gt;<br>
<strong>fluid_settings_setstr</strong> = &lt;CFunctionType object at 0xb70831cc&gt;<br>
<strong>fluid_synth_bank_select</strong> = &lt;CFunctionType object at 0xb708377c&gt;<br>
<strong>fluid_synth_cc</strong> = &lt;CFunctionType object at 0xb70836ac&gt;<br>
<strong>fluid_synth_noteoff</strong> = &lt;CFunctionType object at 0xb70835dc&gt;<br>
<strong>fluid_synth_noteon</strong> = &lt;CFunctionType object at 0xb7083574&gt;<br>
<strong>fluid_synth_pitch_bend</strong> = &lt;CFunctionType object at 0xb7083644&gt;<br>
<strong>fluid_synth_program_change</strong> = &lt;CFunctionType object at 0xb7083714&gt;<br>
<strong>fluid_synth_program_reset</strong> = &lt;CFunctionType object at 0xb708384c&gt;<br>
<strong>fluid_synth_program_select</strong> = &lt;CFunctionType object at 0xb708350c&gt;<br>
<strong>fluid_synth_sfload</strong> = &lt;CFunctionType object at 0xb708343c&gt;<br>
<strong>fluid_synth_sfont_select</strong> = &lt;CFunctionType object at 0xb70837e4&gt;<br>
<strong>fluid_synth_sfunload</strong> = &lt;CFunctionType object at 0xb70834a4&gt;<br>
<strong>fluid_synth_system_reset</strong> = &lt;CFunctionType object at 0xb70838b4&gt;<br>
<strong>fluid_synth_write_s16</strong> = &lt;CFunctionType object at 0xb708391c&gt;<br>
<strong>memmove</strong> = &lt;CFunctionType object at 0xb70d5bf4&gt;<br>
<strong>memset</strong> = &lt;CFunctionType object at 0xb70d5c5c&gt;<br>
<strong>new_fluid_audio_driver</strong> = &lt;CFunctionType object at 0xb7083164&gt;<br>
<strong>new_fluid_settings</strong> = &lt;CFunctionType object at 0xb70d5b8c&gt;<br>
<strong>new_fluid_synth</strong> = &lt;CFunctionType object at 0xb70830fc&gt;<br>
<strong>pydll</strong> = &lt;ctypes.LibraryLoader object at 0xb707592c&gt;<br>
<strong>pythonapi</strong> = &lt;PyDLL 'None', handle b7f58668 at b707594c&gt;</td></tr></table>
</body></html>