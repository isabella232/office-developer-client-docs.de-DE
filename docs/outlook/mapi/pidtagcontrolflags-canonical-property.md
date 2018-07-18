---
title: PidTagControlFlags (kanonische Eigenschaft)
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- PidTagControlFlags
api_type:
- HeaderDef
ms.assetid: b97a9e72-fbb7-49ab-a19d-5e9bd1b8a80d
description: 'Letzte �nderung: Montag, 9. M�rz 2015'
ms.openlocfilehash: f6947efe1aa6866efb7a5a3d96262d021c68013f
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 06/11/2018
ms.locfileid: "19794261"
---
# <a name="pidtagcontrolflags-canonical-property"></a>PidTagControlFlags (kanonische Eigenschaft)

  
  
**Betrifft**: Outlook 
  
Enthält eine Bitmaske aus Flags, die das Verhalten der ein Steuerelement in einem Dialogfeld erstellt aus einer Tabelle anzeigen zum Steuern.
  
|||
|:-----|:-----|
|Zugeordneten Eigenschaften:  <br/> |PR_CONTROL_FLAGS  <br/> |
|Bezeichner:  <br/> |0x3F00  <br/> |
|Datentyp:  <br/> |PT_LONG  <br/> |
|Bereich:  <br/> |Zeigt die MAPI-Tabelle  <br/> |
   
## <a name="remarks"></a>Bemerkungen

Für diese Eigenschaft kann eine oder mehrere der folgenden Werte festgelegt werden:
  
DT_ACCEPT_DBCS 
  
> Das Steuerelement kann Double-Byte-Zeichen (DBCS) Zeichen enthalten. Dieses Kennzeichen werden mit Edit-Steuerelemente verwendet. Es kann mehrere-Byte-Zeichensätze.
    
DT_EDITABLE 
  
> Das Steuerelement bearbeitet werden kann. der Wert mit dem Steuerelement zugeordnet ist, kann geändert werden. Wenn dieses Flag nicht festgelegt ist, ist das Steuerelement schreibgeschützt. Dieser Wert wird ignoriert, Label, Gruppenfeld, standard-Taste, mehrwertigen Dropdown-Listenfeld und Listenfeld-Steuerelemente.
    
DT_MULTILINE 
  
> Das Edit-Steuerelement kann mehrere Zeilen enthalten. Dies bedeutet, dass eine Absatzmarke innerhalb des Steuerelements eingegeben werden kann. Dieses Kennzeichen ist gültig für Bearbeitungssteuerelemente nur.
    
DT_PASSWORD_EDIT 
  
> Bearbeiten von Steuerelementen gilt. Das Edit-Steuerelement wird wie ein Kennwort behandelt. Der Wert wird unter Verwendung von Sternchen anstelle von Echos die eingegebenen Zeichen angezeigt.
    
DT_REQUIRED 
  
> Wenn das Steuerelement Änderungen (DT_EDITABLE) zulässt, muss er einen Wert aufweisen, bevor [IMAPIProp::SaveChanges](imapiprop-savechanges.md) aufgerufen wird. 
    
DT_SET_IMMEDIATE 
  
> Ermöglicht die sofortige Festlegen eines Werts. als ein Wert im Steuerelement geändert wird, ruft MAPI die **SetProps** -Methode für die Eigenschaft im Zusammenhang mit diesem Steuerelement an. Wenn dieses Flag nicht festgelegt ist, werden die Werte festgelegt, wenn das Dialogfeld geschlossen wird. 
    
DT_SET_SELECTION 
  
> Wenn eine Auswahl innerhalb des Listenfelds erfolgt, wird die Indexspalte, Listenfelds als Eigenschaft festgelegt. Immer verwendet mit DT_SET_IMMEDIATE.
    
Diese Eigenschaft wird in den UlCtlFlags Member eines Steuerelements [DTCTL](dtctl.md) Struktur gespeichert. Die meisten die Steuerelement-Kennzeichen gelten für alle Steuerelemente, die von Benutzereingaben zulassen. wenige gelten nur für das Bearbeitungssteuerelement. Steuerelemente, die von Benutzereingaben, wie eine Schaltfläche oder eine Beschriftung, die keine zulassen festgelegt 0 für ihre Flags Steuerelement. 
  
Viele Werte für die Kennzeichen sind selbsterklärend. Beispielsweise wenn DT_REQUIRED für ein Steuerelement festgelegt ist, müssen sie einen Wert enthalten, bevor das Dialogfeld geschlossen werden. Entweder der Dienstanbieter angeben eines Werts durch **IMAPIProp** implementieren, oder der Benutzer kann eine eingeben. DT_EDITABLE gibt an, dass der Wert für das Steuerelement geändert werden kann. DT_MULTILINE können den Wert für ein Edit-Steuerelement über mehrere Zeilen erstrecken. 
  
Einige Steuerelement Flags sind nicht so offensichtlich in ihre Bedeutung. Wenn ein Steuerelement das Flag DT_SET_IMMEDIATE festlegt, wirkt sich auf alle zu dessen Wert, sobald der Benutzer auf ein neues Steuerelement wechselt. MAPI stellt einen einzigen Anruf an die Eigenschaft Schnittstelle [IMAPIProp::SetProps](imapiprop-setprops.md) -Methode für die Eigenschaft des Steuerelements. Dies ist das Standardverhalten besteht darin, dass Änderungen an Steuerelementwerte wirksam erst, nachdem der Benutzer die Schaltfläche **OK wählt** oder das Dialogfeld schließt verschieben unterscheidet. Das Flag DT_SET_IMMEDIATE wird häufig in Kombination mit anzeigebenachrichtigungen-Tabelle verwendet. 
  
Die folgende Tabelle enthält die Typen von Steuerelementen und alle Werte für die Kennzeichen, die für jeden Typ festgelegt werden können.
  
|**Control**|**Gültige Werte für diese Eigenschaft**|
|:-----|:-----|
|Schaltfläche  <br/> |Muss 0 (null)  <br/> |
|Kontrollkästchen  <br/> |DT_EDITABLE DT_SET_IMMEDIATE  <br/> |
|Kombinationsfeld  <br/> |DT_EDITABLE, DT_REQUIRED, DT_SET_IMMEDIATE  <br/> |
|Dropdown-Listenfeld  <br/> |DT_EDITABLE DT_SET_IMMEDIATE  <br/> |
|Bearbeiten  <br/> |DT_ACCEPT_DBCS, DT_MULTILINE, DT_EDITABLE, DT_PASSWORD_EDIT, DT_REQUIRED, DT_SET_IMMEDIATE  <br/> |
|Gruppenfeld  <br/> |Muss 0 (null)  <br/> |
|Beschriftung  <br/> |Muss 0 (null)  <br/> |
|Listenfeld  <br/> |Muss 0 (null)  <br/> |
|Mehrwertige Dropdown-Listenfeld  <br/> |Muss 0 (null)  <br/> |
|Mehrwertige Listenfeld  <br/> |Muss 0 (null)  <br/> |
|Seite mit Registerkarten  <br/> |Muss 0 (null)  <br/> |
|Optionsfeld  <br/> |Muss 0 (null)  <br/> |
   
## <a name="related-resources"></a>Verwandte Ressourcen

### <a name="header-files"></a>Header-Dateien

Mapidefs.h
  
> Enthält die Datentypdefinitionen.
    
Mapitags.h
  
> Enthält Definitionen von Eigenschaften, die als Alternative Namen aufgelistet.
    
## <a name="see-also"></a>Siehe auch



[MAPI-Eigenschaften](mapi-properties.md)
  
[Kanonische MAPI-Eigenschaften](mapi-canonical-properties.md)
  
[Zuordnen von kanonischen Eigenschaftennamen zu MAPI-Namen](mapping-canonical-property-names-to-mapi-names.md)
  
[Zuordnen von MAPI-Namen zu kanonische Eigenschaftennamen](mapping-mapi-names-to-canonical-property-names.md)

