DayZ "Mummies Spawn At Castles" XML Mod For Consoles & PC XML Snippets Instructions & Terms Of Use

These snippets will spawn in the Mummy Infected Zombie ( ZmbM_Mummy ) at various Castles & Castle Ruins around Chernarus.

WARNING! THESE INFECTED ARE VERY DIFFICULT TO KILL!!!!!

Limited Testing on PC Chernarus Local Server DAYZ Version 1.20 Mar 2023.

XML Snippets Created by @scalespeeder. Please report bugs & errors to scalespeeder@gmail.com with screenshots.

TERMS OF USE
THE SOFTWARE IS PROVIDED "AS IS", WITHOUT WARRANTY OF ANY KIND,
EXPRESS OR IMPLIED, INCLUDING BUT NOT LIMITED TO THE WARRANTIES OF MERCHANTABILITY,
FITNESS FOR A PARTICULAR PURPOSE AND NONINFRINGEMENT. IN NO EVENT SHALL THE AUTHORS
OR COPYRIGHT HOLDERS BE LIABLE FOR ANY CLAIM, DAMAGES OR OTHER LIABILITY, WHETHER IN
AN ACTION OF CONTRACT, TORT OR OTHERWISE, ARISING FROM, OUT OF OR IN CONNECTION WITH
THE SOFTWARE OR THE USE OR OTHER DEALINGS IN THE SOFTWARE.

Using these modded xml / json files and instructions could break the functioning of your DAYZ server, requiring a reinstall that would wipe
all player progress.

Using these modded files neccessitates increased regular restarts to prevent server crashing.

It is suggested you thoroughly test your server after applying these files to ensure proper
functioning of your server.

I always recomend you validate your files at: https://www.xmlvalidation.com/ and https://jsonformatter.curiousconcept.com/

Instructions:

This snippet should be inserted into your missions types.xml:

<!-- mummys at castle types entry-->

 <type name="ZmbM_Mummy">
        <nominal>0</nominal>
        <lifetime>1800</lifetime>
        <restock>0</restock>
        <min>1</min>
        <quantmin>-1</quantmin>
        <quantmax>-1</quantmax>
        <cost>100</cost>
        <flags count_in_cargo="0" count_in_hoarder="0" count_in_map="1" count_in_player="0" crafted="0" deloot="0"/>
    </type>

<!-- mummys at castle end -->
	
	
This code snippet should be inserted into your events.xml file :
	
	<!-- mummys at castle events entry-->
	
	    <event name="InfectedCastle">
        <nominal>50</nominal>
        <min>25</min>
        <max>100</max>
        <lifetime>3</lifetime>
        <restock>0</restock>
        <saferadius>100</saferadius>
        <distanceradius>50</distanceradius>
        <cleanupradius>100</cleanupradius>
        <flags deletable="0" init_random="0" remove_damaged="1"/>
        <position>player</position>
        <limit>custom</limit>
        <active>1</active>
        <children>
            <child lootmax="3" lootmin="0" max="0" min="100" type="ZmbM_Mummy"/>
        </children>
    </event>
	
	<!-- mummys at castle end -->
	

Add this code snippet to your cfgspawnabletypes.xml:

	<!-- mummy cfgspawnabletypes entry -->

	<type name="ZmbM_Mummy">
		<cargo preset="ContaminatedCargo" />
		<cargo chance="0.05">
			<item name="AntiChemInjector" chance="1.0" />
		</cargo>
		<cargo chance="0.5">
			<item name="HumanSteakMeat" chance="1.0" />
		</cargo>
		<cargo chance="0.5">
			<item name="BandageDressing" chance="0.5" />
			<item name="Rag" chance="0.5" />
		</cargo>
		<cargo chance="0.5">
			<item name="IodineTincture" chance="0.33" />
			<item name="Epinephrine" chance="0.33" />
			<item name="Morphine" chance="0.33" />
		</cargo>
		<cargo chance="0.5">
			<item name="CharcoalTablets" chance="0.25" />
			<item name="PainkillerTablets" chance="0.25" />
			<item name="TetracyclineAntibiotics" chance="0.25" />
			<item name="VitaminBottle" chance="0.25" />
		</cargo>
	</type>
	
	<!-- end of mummy cfgspawnabletypes entry -->
	
Add this code snippet to your zombie_territories.xml :

<!-- mummys at castle zombie territories entry-->

 <territory color="1136576269">
        <zone name="InfectedCastle" 	smin="1" smax="1" dmin="0" dmax="0" x="6554.89" z="5612.14" r="60"/> 
        <zone name="InfectedCastle" 	smin="1" smax="1" dmin="0" dmax="0" x="6913.05" z="11376.50" r="140"/>
        <zone name="InfectedCastle" 	smin="1" smax="1" dmin="0" dmax="0" x="6879.56" z="11491.69" r="120"/>
        <zone name="InfectedCastle" 	smin="1" smax="1" dmin="0" dmax="0" x="10278.76" z="12053.40" r="70"/>  
        <zone name="InfectedCastle" 	smin="1" smax="1" dmin="0" dmax="0" x="1417.17" z="9258.70" r="120"/> 
        <zone name="InfectedCastle" 	smin="1" smax="1" dmin="0" dmax="0" x="1437.84" z="9221.45" r="70"/>
		<zone name="InfectedCastle" 	smin="1" smax="1" dmin="0" dmax="0" x="13497.35" z="3301.73" r="140"/>
        <zone name="InfectedCastle" 	smin="1" smax="1" dmin="0" dmax="0" x="13422.18" z="3287.93" r="120"/> 
        <zone name="InfectedCastle" 	smin="1" smax="1" dmin="0" dmax="0" x="11246.05" z="4295.07" r="70"/> 
        <zone name="InfectedCastle" 	smin="1" smax="1" dmin="0" dmax="0" x="9302.82" z="13506.66" r="120"/> 
        <zone name="InfectedCastle" 	smin="1" smax="1" dmin="0" dmax="0" x="7418.32" z="9115.28" r="70"/>  
</territory>

<!-- mummys at castle end -->

	
Save and re-upload if necessary and re-start your server for the changes to take effect.

Thanks, Rob.