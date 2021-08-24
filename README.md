# Cod4-HelicopterFastRope
Voila un tuto sur comment faire que des ia s'héliporte via un hélico ! 




# Via L'éditeur 


Premièrement placez un hélico sur votre map en cliquant sur la zone 2D de l'éditeur (Partis à gauche)

Puis # script > model

Puis séléctionner le model **vehicle_mi17_woodland_fly**

**Seulement tester avec le mi17**

Une fois l'hélico placez séléctionner l'hélico avec <kbd>SHIFT</kbd> + Clique Gauche sur l'hélico

Puis Appuyer sur N pour ouvrir le menu des entité 

Puis ajouter ceci

(Ne mettez pas KEY et VALUE j'ai mis ça pour vous permettre de vous réperer pour savoir ou mettre les différente informations !)



KEY      script_noteworthy
Value    my_chopper

KEY      script_startinghealth
Value    5


KEY      script_vehicleride
Value    0

KEY      script_vehiclespawngroup
Value    0

KEY     speed
Value   15



# Voila maintenant que vous avez fait cela il est maintenant temps de placer les ia alliès ou ennemis qui seront dans l'hélico !

Placer 8 ia alliès ou ennemis !

Une fois fait séléctionnez les puis appuyer sur N pour r'ouvrir le menu des Entity !

Puis cocher la case SPAWNER !

Désormais  appuyer sur <kbd>SHIFT</kbd> + V  (AVEC LES IA SELECTIONNER !)

Puis appuyez sur **Ride ON/In Vehicle !**


# Maintenant passons au code !

Allez dans le .gsc de votre map 


et mettez si ce code (code trouvable dans le github :)  )

```gsc

maps\_mi17::main( "vehicle_mi17_woodland_fly" ); // Nécessaire pour l'hélicoptére !

	thread maps\_vehicle::create_vehicle_from_spawngroup_and_gopath( 0 );


```


Puis allez dans le CODCOMPILER puis dans **Update Zone File**

Puis collez y ceci:

```

xanim,fastrope_fall
xanim,fastrope_fall
xanim,mi17_8_drop
xanim,mi17_8_idle
xanim,mi17_7_drop
xanim,mi17_7_idle
xanim,mi17_6_drop
xanim,mi17_6_idle
xanim,mi17_5_drop
xanim,mi17_5_idle
xanim,mi17_4_drop
xanim,mi17_4_idle
xanim,mi17_3_drop
xanim,mi17_3_idle
xanim,mi17_2_drop
xanim,mi17_2_idle
xanim,mi17_1_idle
xanim,mi17_1_drop
xanim,helicopter_pilot2_twitch_radio
xanim,helicopter_pilot2_twitch_lookoutside
xanim,helicopter_pilot2_twitch_clickpannel
xanim,helicopter_pilot2_idle
xanim,helicopter_pilot1_twitch_lookoutside
xanim,helicopter_pilot1_twitch_lookback
xanim,helicopter_pilot1_twitch_clickpannel
xanim,helicopter_pilot1_idle
xanim,mi17_rope_drop_ri
xanim,mi17_rope_idle_ri
xanim,mi17_rope_drop_le
xanim,mi17_rope_idle_le
xanim,mi17_heli_rotors
xanim,mi17_heli_idle
xmodel,vehicle_mi17_woodland_fly
xmodel,rope_test_ri
xmodel,rope_test
fx,fire/fire_smoke_trail_l
fx,explosions/aerial_explosion
fx,explosions/helicopter_explosion_mi17_woodland_low
fx,misc/aircraft_light_cockpit_red
fx,misc/aircraft_light_cockpit_blue
fx,misc/aircraft_light_white_blink
fx,misc/aircraft_light_red_blink
fx,misc/aircraft_light_wingtip_green
fx,misc/aircraft_light_wingtip_red




```

# Maintenant compiler votre map Cliquez sur Rebuild Fast File et lancez votre map enjoy !






