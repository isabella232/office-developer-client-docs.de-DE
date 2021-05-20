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
description: 'Letzte Änderung: Montag, 9. März 2015'
ms.openlocfilehash: 099f08876eadc83ebb66b9e4226eeeee6277bf01
ms.sourcegitcommit: 8657170d071f9bcf680aba50b9c07f2a4fb82283
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 04/28/2019
ms.locfileid: "33430882"
---
# <a name="pidtagcontrolflags-canonical-property"></a>PidTagControlFlags (kanonische Eigenschaft)

  
  
**Gilt für**: Outlook 2013 | Outlook 2016 
  
Enthält eine Bitmaske mit Flags, die das Verhalten eines Steuerelements steuern, das in einem Dialogfeld verwendet wird, das aus einer Anzeigetabelle erstellt wurde.
  
|||
|:-----|:-----|
|Zugeordnete Eigenschaften:  <br/> |PR_CONTROL_FLAGS  <br/> |
|Kennung:  <br/> |0x3F00  <br/> |
|Datentyp:  <br/> |PT_LONG  <br/> |
|Bereich:  <br/> |MAPI-Anzeigetabelle  <br/> |
   
## <a name="remarks"></a>Hinweise

Mindestens eines der folgenden Kennzeichen kann für diese Eigenschaft festgelegt werden:
  
DT_ACCEPT_DBCS 
  
> Das Steuerelement kann Double-Byte Zeichensatz (Character Set, DBCS) enthalten. Dieses Flag wird mit Bearbeitungssteuerelementen verwendet. Sie ermöglicht Mehrere-Byte-Zeichensätze.
    
DT_EDITABLE 
  
> Das Steuerelement kann bearbeitet werden. der dem Steuerelement zugeordnete Wert kann geändert werden. Wenn dieses Flag nicht festgelegt ist, ist das Steuerelement schreibgeschützt. Dieser Wert wird für Bezeichnungs-, Gruppenfeld-, Standard-Pushschaltfläche, mehrwertige Dropdownlistenfeld- und Listenfeldsteuerelemente ignoriert.
    
DT_MULTILINE 
  
> Das Bearbeitungssteuerelement kann mehrere Zeilen enthalten. Dies bedeutet, dass innerhalb des Steuerelements ein Rückgabezeichen eingegeben werden kann. Dieses Flag ist nur für Bearbeitungssteuerelemente gültig.
    
DT_PASSWORD_EDIT 
  
> Gilt für Bearbeitungssteuerelemente. Das Bearbeitungssteuerelement wird wie ein Kennwort behandelt. Der Wert wird mithilfe von Sternchen angezeigt, anstatt die tatsächlich eingegebenen Zeichen zu echosen.
    
DT_REQUIRED 
  
> Wenn das Steuerelement Änderungen zulässt (DT_EDITABLE), muss es einen Wert haben, bevor [IMAPIProp::SaveChanges](imapiprop-savechanges.md) aufgerufen wird. 
    
DT_SET_IMMEDIATE 
  
> Ermöglicht das sofortige Festlegen eines Werts. Sobald sich ein Wert im Steuerelement ändert, ruft MAPI die **SetProps-Methode** für die diesem Steuerelement zugeordnete Eigenschaft auf. Wenn dieses Flag nicht festgelegt ist, werden die Werte festgelegt, wenn das Dialogfeld nicht mehr angezeigt wird. 
    
DT_SET_SELECTION 
  
> Wenn innerhalb des Listenfelds eine Auswahl getroffen wird, wird die Indexspalte dieses Listenfelds als Eigenschaft festgelegt. Wird immer mit DT_SET_IMMEDIATE.
    
Diese Eigenschaft wird im ulCtlFlags-Element der [DTCTL-Struktur](dtctl.md) eines Steuerelements gespeichert. Die meisten Steuerelementflags gelten für alle Steuerelemente, die Benutzereingaben zulassen. einige gelten nur für das Bearbeitungssteuerelement. Steuerelemente, die keine Benutzereingaben zulassen, z. B. eine Schaltfläche oder eine Bezeichnung, legen 0 für ihre Steuerelementflags fest. 
  
Viele der Kennzeichenwerte sind selbsterklärend. Wenn z. B. DT_REQUIRED für ein Steuerelement festgelegt ist, muss es einen Wert enthalten, bevor das Dialogfeld verworfen werden kann. Entweder kann der Dienstanbieter einen Wert über seine **IMAPIProp-Implementierung** liefern, oder der Benutzer kann einen Wert eingeben. DT_EDITABLE gibt an, dass der Wert für das Steuerelement geändert werden kann. DT_MULTILINE kann der Wert für ein Bearbeitungssteuerelement mehrere Zeilen umfassen. 
  
Einige Steuerelementflags sind in ihrer Bedeutung nicht so offensichtlich. Wenn ein Steuerelement das DT_SET_IMMEDIATE, wirken sich alle Änderungen an seinem Wert aus, sobald der Benutzer zu einem neuen Steuerelement wechselt. MAPI macht einen einzelnen Aufruf der [IMAPIProp::SetProps-Methode](imapiprop-setprops.md) der Eigenschaft des Steuerelements. Dies ist anders als das Standardverhalten, bei dem Änderungen an Steuerelementwerten erst wirksam werden, wenn der Benutzer die Schaltfläche **OK** auswählt oder das Dialogfeld schließt. Das DT_SET_IMMEDIATE wird häufig in Kombination mit Anzeigetabelle Benachrichtigungen verwendet. 
  
In der folgenden Tabelle sind die Typen von Steuerelementen und alle Kennzeichenwerte aufgeführt, die für jeden Typ festgelegt werden können.
  
|**Control**|**Gültige Werte für diese Eigenschaft**|
|:-----|:-----|
|Schaltfläche  <br/> |Muss null sein  <br/> |
|Kontrollkästchen  <br/> |DT_EDITABLE, DT_SET_IMMEDIATE  <br/> |
|Kombinationsfeld  <br/> |DT_EDITABLE, DT_REQUIRED, DT_SET_IMMEDIATE  <br/> |
|Dropdownlistenfeld  <br/> |DT_EDITABLE, DT_SET_IMMEDIATE  <br/> |
|Bearbeiten  <br/> |DT_ACCEPT_DBCS, DT_MULTILINE, DT_EDITABLE, DT_PASSWORD_EDIT, DT_REQUIRED, DT_SET_IMMEDIATE  <br/> |
|Gruppenfeld  <br/> |Muss null sein  <br/> |
|Bezeichnung  <br/> |Muss null sein  <br/> |
|Listenfeld  <br/> |Muss null sein  <br/> |
|Dropdownlistenfeld für mehrwertige Werte  <br/> |Muss null sein  <br/> |
|Listenfeld mit mehreren Bewertungswerten  <br/> |Muss null sein  <br/> |
|Registerkartenseite  <br/> |Muss null sein  <br/> |
|Optionsfeld  <br/> |Muss null sein  <br/> |
   
## <a name="related-resources"></a>Verwandte Ressourcen

### <a name="header-files"></a>Headerdateien

Mapidefs.h
  
> Bietet Datentypdefinitionen.
    
Mapitags.h
  
> Enthält Definitionen von Eigenschaften, die als alternative Namen aufgeführt sind.
    
## <a name="see-also"></a>Siehe auch



[MAPI-Eigenschaften](mapi-properties.md)
  
[KANONISCHE EIGENSCHAFTEN VON MAPI](mapi-canonical-properties.md)
  
[Zuordnen kanonischer Eigenschaftsnamen zu MAPI-Namen](mapping-canonical-property-names-to-mapi-names.md)
  
[Zuordnen von MAPI-Namen zu kanonischen Eigenschaftennamen](mapping-mapi-names-to-canonical-property-names.md)

