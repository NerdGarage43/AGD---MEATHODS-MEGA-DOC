# AGD---MEATHODS-MEGA-DOC

=== AGD.ModAPI.IModPlayer ===
  [Method] T GetPerk[T]()
  [Method] Boolean HasPerk[T]()

=== AGD.ModAPI.ModEventBus ===
  [Event] System.Action`1[AGD.ModAPI.DamageEvent] OnDealDamage
  [Event] System.Action`1[AGD.ModAPI.ItemAcquiredEvent] OnItemAcquired
  [Event] System.Action`1[AGD.ModAPI.KillEvent] OnKill
  [Event] System.Action`1[AGD.ModAPI.PerkAcquiredEvent] OnPerkAcquired
  [Event] System.Action`1[AGD.ModAPI.RoundEvent] OnPerkSelectionStart
  [Event] System.Action`1[AGD.ModAPI.RoundEvent] OnRoundEnd
  [Event] System.Action`1[AGD.ModAPI.RoundEvent] OnRoundStart
  [Event] System.Action`1[AGD.ModAPI.DamageEvent] OnTakeDamage
  [Method] Void add_OnDealDamage(System.Action`1[AGD.ModAPI.DamageEvent])
  [Method] Void add_OnItemAcquired(System.Action`1[AGD.ModAPI.ItemAcquiredEvent])
  [Method] Void add_OnKill(System.Action`1[AGD.ModAPI.KillEvent])
  [Method] Void add_OnPerkAcquired(System.Action`1[AGD.ModAPI.PerkAcquiredEvent])
  [Method] Void add_OnPerkSelectionStart(System.Action`1[AGD.ModAPI.RoundEvent])
  [Method] Void add_OnRoundEnd(System.Action`1[AGD.ModAPI.RoundEvent])
  [Method] Void add_OnRoundStart(System.Action`1[AGD.ModAPI.RoundEvent])
  [Method] Void add_OnTakeDamage(System.Action`1[AGD.ModAPI.DamageEvent])
  [Method] Boolean Equals(System.Object)
  [Method] Int32 GetHashCode()
  [Method] System.Type GetType()
  [Method] Void remove_OnDealDamage(System.Action`1[AGD.ModAPI.DamageEvent])
  [Method] Void remove_OnItemAcquired(System.Action`1[AGD.ModAPI.ItemAcquiredEvent])
  [Method] Void remove_OnKill(System.Action`1[AGD.ModAPI.KillEvent])
  [Method] Void remove_OnPerkAcquired(System.Action`1[AGD.ModAPI.PerkAcquiredEvent])
  [Method] Void remove_OnPerkSelectionStart(System.Action`1[AGD.ModAPI.RoundEvent])
  [Method] Void remove_OnRoundEnd(System.Action`1[AGD.ModAPI.RoundEvent])
  [Method] Void remove_OnRoundStart(System.Action`1[AGD.ModAPI.RoundEvent])
  [Method] Void remove_OnTakeDamage(System.Action`1[AGD.ModAPI.DamageEvent])
  [Method] System.String ToString()

=== AGD.ModAPI.DamageEvent ===
  [Field] AGD.ModAPI.IModPlayer Attacker
  [Field] DamageSource Source
  [Field] AGD.ModAPI.IModPlayer Victim
  [Method] Boolean Equals(System.Object)
  [Method] Single get_Damage()
  [Method] Items.Item get_SourceItem()
  [Method] Int32 GetHashCode()
  [Method] System.Type GetType()
  [Method] Void set_Damage(Single)
  [Method] Boolean SourceItemHasTag(System.String)
  [Method] System.String ToString()
  [Property] Single Damage
  [Property] Items.Item SourceItem

=== AGD.ModAPI.KillEvent ===
  [Field] AGD.ModAPI.IModPlayer Killer
  [Field] DamageSource Source
  [Field] AGD.ModAPI.IModPlayer Victim
  [Method] Boolean Equals(System.Object)
  [Method] Items.Item get_SourceItem()
  [Method] Int32 GetHashCode()
  [Method] System.Type GetType()
  [Method] System.String ToString()
  [Property] Items.Item SourceItem

=== AGD.ModAPI.RoundEvent ===
  [Field] Int32 RoundNumber
  [Method] Boolean Equals(System.Object)
  [Method] Int32 GetHashCode()
  [Method] System.Type GetType()
  [Method] System.String ToString()

=== AGD.ModAPI.PerkAcquiredEvent ===
  [Field] Game.Perk Perk
  [Field] AGD.ModAPI.IModPlayer Player
  [Method] Boolean Equals(System.Object)
  [Method] Int32 GetHashCode()
  [Method] System.Type GetType()
  [Method] System.String ToString()

=== AGD.ModAPI.ItemAcquiredEvent ===
  [Field] Items.Item Item
  [Field] AGD.ModAPI.IModPlayer Player
  [Method] Boolean Equals(System.Object)
  [Method] Int32 GetHashCode()
  [Method] System.Type GetType()
  [Method] System.String ToString()

=== AGD.ModAPI.IModContext ===
  [Method] AGD.ModAPI.ModEventBus get_Events()
  [Method] System.String get_InstallPath()
  [Method] System.String get_ModId()
  [Method] Void RegisterPerk(System.String, UnityEngine.ScriptableObject, AGD.ModAPI.ModPerkMetadata)
  [Method] Items.Item TryGetRandomItem()
  [Method] Boolean TryGiveItem(AGD.ModAPI.IModPlayer, Items.Item, Boolean)
  [Method] Boolean TryGivePerk(AGD.ModAPI.IModPlayer, Game.Perk)
  [Method] Boolean TrySpawnCannon(UnityEngine.Vector3, UnityEngine.Quaternion)
  [Method] Boolean TrySpawnItemPickup(UnityEngine.Vector3, Items.Item, Single)
  [Property] AGD.ModAPI.ModEventBus Events
  [Property] System.String InstallPath
  [Property] System.String ModId

=== Game.Perk ===
  [Field] Availability availability
  [Field] Single chanceModifier
  [Field] Boolean dontIncludeInPool
  [Field] UnityEngine.Sprite icon
  [Field] Boolean isConsumable
  [Field] Game.PerkCategory perkCategory
  [Field] UnityEngine.Localization.LocalizedString translatedDesc
  [Field] UnityEngine.Localization.LocalizedString translatedTitle
  [Field] PerkValueCategory valueCategory
  [Method] Boolean Equals(System.Object)
  [Method] Boolean get_active()
  [Method] UnityEngine.HideFlags get_hideFlags()
  [Method] System.String get_name()
  [Method] Int32 GetHashCode()
  [Method] Int32 GetInstanceID()
  [Method] System.Type GetType()
  [Method] Void InitState(HeldPerk)
  [Method] Game.IDynamicPerkUI RenderUI(UI.Game.PerkCardUI, HeldPerk)
  [Method] Void set_hideFlags(UnityEngine.HideFlags)
  [Method] Void set_name(System.String)
  [Method] Void SetDirty()
  [Method] Boolean ShouldShowInDeck(Player.PlayerController)
  [Method] System.String ToString()
  [Method] Void UpdateUI(UI.Game.PerkCardUI, Player.PlayerController, HeldPerk, Game.IDynamicPerkUI)
  [Property] Boolean active
  [Property] UnityEngine.HideFlags hideFlags
  [Property] System.String name

Done.

