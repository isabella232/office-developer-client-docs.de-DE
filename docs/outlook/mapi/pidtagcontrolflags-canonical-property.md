---
title: Kanonische PidTagControlFlags-Eigenschaft
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
ms.localizationpriority: medium
api_name:
- PidTagControlFlags
api_type:
- HeaderDef
ms.assetid: b97a9e72-fbb7-49ab-a19d-5e9bd1b8a80d
description: 'Letzte Änderung: Montag, 9. März 2015'
ms.openlocfilehash: fdfa27d06dcfb3542c03575b51b6483410266985
ms.sourcegitcommit: a1d9041c20256616c9c183f7d1049142a7ac6991
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 09/24/2021
ms.locfileid: "59613618"
---
# <a name="pidtagcontrolflags-canonical-property"></a>Kanonische PidTagControlFlags-Eigenschaft

  
  
**Gilt für**: Outlook 2013 | Outlook 2016 
  
Enthält eine Bitmaske mit Flags, die das Verhalten eines Steuerelements steuern, das in einem dialogfeld verwendet wird, das aus einer Anzeigetabelle erstellt wurde.
  
|||
|:-----|:-----|
|Zugeordnete Eigenschaften:  <br/> |PR_CONTROL_FLAGS  <br/> |
|Kennung:  <br/> |0x3F00  <br/> |
|Datentyp:  <br/> |PT_LONG  <br/> |
|Bereich:  <br/> |MAPI-Anzeigetabelle  <br/> |
   
## <a name="remarks"></a>Bemerkungen

Mindestens eines der folgenden Flags kann für diese Eigenschaft festgelegt werden:
  
DT_ACCEPT_DBCS 
  
> Das Steuerelement kann Double-Byte Zeichensatzzeichen (Character Set, DBCS) enthalten. Dieses Kennzeichen wird mit Bearbeitungssteuerelementen verwendet. Sie ermöglicht Mehrere-Byte-Zeichensätze.
    
DT_EDITABLE 
  
> Das Steuerelement kann bearbeitet werden. Der dem Steuerelement zugeordnete Wert kann geändert werden. Wenn dieses Kennzeichen nicht festgelegt ist, ist das Steuerelement schreibgeschützt. Dieser Wert wird für Bezeichnungsfelder, Gruppenfelder, Standard-Schaltflächen, mehrwertige Dropdownlistenfelder und Listenfeld-Steuerelemente ignoriert.
    
DT_MULTILINE 
  
> Das Bearbeitungssteuerelement kann mehrere Zeilen enthalten. Dies bedeutet, dass ein Rückgabezeichen in das Steuerelement eingegeben werden kann. Dieses Kennzeichen ist nur für Bearbeitungssteuerelemente gültig.
    
DT_PASSWORD_EDIT 
  
> Gilt für Bearbeitungssteuerelemente. Das Bearbeitungssteuerelement wird wie ein Kennwort behandelt. Der Wert wird mit Sternchen angezeigt, anstatt die tatsächlich eingegebenen Zeichen zu wiederholen.
    
DT_REQUIRED 
  
> Wenn das Steuerelement Änderungen zulässt (DT_EDITABLE), muss es einen Wert aufweisen, bevor [IMAPIProp::SaveChanges](imapiprop-savechanges.md) aufgerufen wird. 
    
DT_SET_IMMEDIATE 
  
> Aktiviert die sofortige Einstellung eines Werts. Sobald sich ein Wert im Steuerelement ändert, ruft MAPI die **SetProps-Methode** für die diesem Steuerelement zugeordnete Eigenschaft auf. Wenn dieses Kennzeichen nicht festgelegt ist, werden die Werte festgelegt, wenn das Dialogfeld geschlossen wird. 
    
DT_SET_SELECTION 
  
> Wenn innerhalb des Listenfelds eine Auswahl getroffen wird, wird die Indexspalte dieses Listenfelds als Eigenschaft festgelegt. Wird immer mit DT_SET_IMMEDIATE verwendet.
    
Diese Eigenschaft wird im ulCtlFlags-Element der [DTCTL-Struktur](dtctl.md) eines Steuerelements gespeichert. Die meisten Steuerelementkennzeichen gelten für alle Steuerelemente, die Benutzereingaben zulassen. Einige wenige gelten nur für das Bearbeitungssteuerelement. Steuerelemente, die keine Benutzereingaben zulassen, z. B. eine Schaltfläche oder eine Beschriftung, legen 0 für ihre Steuerelementflags fest. 
  
Viele der Kennzeichenwerte sind selbsterklärend. Wenn beispielsweise DT_REQUIRED für ein Steuerelement festgelegt ist, muss es einen Wert enthalten, bevor das Dialogfeld geschlossen werden kann. Entweder kann der Dienstanbieter einen Wert über seine **IMAPIProp-Implementierung** bereitstellen, oder der Benutzer kann einen eingeben. DT_EDITABLE gibt an, dass der Wert für das Steuerelement geändert werden kann. DT_MULTILINE lässt zu, dass sich der Wert eines Bearbeitungssteuerelements über mehrere Zeilen erstreckt. 
  
Einige Steuerelementkennzeichen sind in ihrer Bedeutung nicht so offensichtlich. Wenn ein Steuerelement das DT_SET_IMMEDIATE Flag festlegt, wirken sich alle Änderungen an seinem Wert auf das neue Steuerelement aus, sobald der Benutzer zu einem neuen Steuerelement wechselt. MAPI führt einen einzelnen Aufruf der [IMAPIProp::SetProps-Methode](imapiprop-setprops.md) der Eigenschaftenschnittstelle für die Eigenschaft des Steuerelements durch. Dies unterscheidet sich vom Standardverhalten, das darin besteht, zu verschieben, dass Änderungen an Steuerelementwerten wirksam werden, bis der Benutzer die **SCHALTFLÄCHE "OK"** auswählt oder das Dialogfeld schließt. Das DT_SET_IMMEDIATE Flag wird häufig in Kombination mit Anzeigetabellenbenachrichtigungen verwendet. 
  
In der folgenden Tabelle sind die Typen von Steuerelementen und alle Kennzeichenwerte aufgeführt, die für jeden Typ festgelegt werden können.
  
|**Control**|**Gültige Werte für diese Eigenschaft**|
|:-----|:-----|
|Schaltfläche  <br/> |Muss Null sein  <br/> |
|Kontrollkästchen  <br/> |DT_EDITABLE, DT_SET_IMMEDIATE  <br/> |
|Kombinationsfeld  <br/> |DT_EDITABLE, DT_REQUIRED, DT_SET_IMMEDIATE  <br/> |
|Dropdown-Listenfeld  <br/> |DT_EDITABLE, DT_SET_IMMEDIATE  <br/> |
|Bearbeiten  <br/> |DT_ACCEPT_DBCS, DT_MULTILINE, DT_EDITABLE, DT_PASSWORD_EDIT, DT_REQUIRED, DT_SET_IMMEDIATE  <br/> |
|Gruppenfeld  <br/> |Muss Null sein  <br/> |
|Beschriftung  <br/> |Muss Null sein  <br/> |
|Listenfeld  <br/> |Muss Null sein  <br/> |
|Dropdown-Listenfeld mit mehreren Werten  <br/> |Muss Null sein  <br/> |
|Mehrwertiges Listenfeld  <br/> |Muss Null sein  <br/> |
|Registerkartenseite  <br/> |Muss Null sein  <br/> |
|Optionsfeld  <br/> |Muss Null sein  <br/> |
   
## <a name="related-resources"></a>Verwandte Ressourcen

### <a name="header-files"></a>Headerdateien

Mapidefs.h
  
> Stellt Datentypdefinitionen bereit.
    
Mapitags.h
  
> Enthält Definitionen von Eigenschaften, die als alternative Namen aufgelistet sind.
    
## <a name="see-also"></a>Siehe auch



[MAPI-Eigenschaften](mapi-properties.md)
  
[KANonische MAPI-Eigenschaften](mapi-canonical-properties.md)
  
[Zuordnen kanonischer Eigenschaftennamen zu MAPI-Namen](mapping-canonical-property-names-to-mapi-names.md)
  
[Zuordnen von MAPI-Namen zu kanonischen Eigenschaftsnamen](mapping-mapi-names-to-canonical-property-names.md)

