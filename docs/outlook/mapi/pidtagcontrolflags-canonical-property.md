---
title: Kanonische Pidtagcontrolflags (-Eigenschaft
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
ms.openlocfilehash: 099f08876eadc83ebb66b9e4226eeeee6277bf01
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 04/23/2019
ms.locfileid: "32331864"
---
# <a name="pidtagcontrolflags-canonical-property"></a>Kanonische Pidtagcontrolflags (-Eigenschaft

  
  
**Gilt für**: Outlook 2013 | Outlook 2016 
  
Enthält eine Bitmaske von Flags, die das Verhalten eines Steuerelements steuern, das in einem von einer Anzeigetabelle erstellten Dialogfeldverwendet wird.
  
|||
|:-----|:-----|
|Zugeordnete Eigenschaften:  <br/> |PR_CONTROL_FLAGS  <br/> |
|Kennung:  <br/> |0x3F00  <br/> |
|Datentyp:  <br/> |PT_LONG  <br/> |
|Bereich:  <br/> |MAPI-Anzeigetabelle  <br/> |
   
## <a name="remarks"></a>Bemerkungen

Mindestens eines der folgenden Flags kann für diese Eigenschaft festgelegt werden:
  
DT_ACCEPT_DBCS 
  
> Das Steuerelement kann Double-Byte Character Set (DBCS)-Zeichen enthalten. Dieses Flag wird mit Bearbeitungssteuerelementen verwendet. Es ermöglicht mehr Byte-Zeichensätze.
    
DT_EDITABLE 
  
> Das Steuerelement kann bearbeitet werden; der Wert, der dem Steuerelement zugeordnet ist, kann geändert werden. Wenn dieses Flag nicht festgelegt ist, ist das Steuerelement schreibgeschützt. Dieser Wert wird bei Bezeichnung, Gruppenfeld, Standard-Schaltflächen, mehrwertigen Dropdown-Listenfeldern und Listenfeld-Steuerelementen ignoriert.
    
DT_MULTILINE 
  
> Das Bearbeitungssteuerelement kann mehrere Zeilen enthalten. Dies gibt an, dass ein Rückgabe Zeichen innerhalb des Steuerelements eingegeben werden kann. Dieses Flag ist nur für Bearbeitungssteuerelemente gültig.
    
DT_PASSWORD_EDIT 
  
> Gilt für Bearbeitungssteuerelemente. Das Bearbeitungssteuerelement wird wie ein Kennwort behandelt. Der Wert wird mit Sternchen angezeigt, statt die eingegebenen tatsächlichen Zeichen wiederzugeben.
    
DT_REQUIRED 
  
> Wenn das Steuerelementänderungen (DT_EDITABLE) zulässt, muss es einen Wert aufweisen, bevor [IMAPIProp:: SaveChanges](imapiprop-savechanges.md) aufgerufen wird. 
    
DT_SET_IMMEDIATE 
  
> Ermöglicht die sofortige Einstellung eines Werts; Sobald ein Wert im Steuerelement geändert wird, ruft MAPI die setProps-Methode für die Eigenschaft auf, die diesem Steuerelement zugeordnet ist. **** Wenn dieses Flag nicht festgelegt ist, werden die Werte festgelegt, wenn das Dialogfeld geschlossen wird. 
    
DT_SET_SELECTION 
  
> Wenn im Listenfeld eine Auswahl vorgenommen wird, wird die Indexspalte des Listenfelds als Eigenschaft festgelegt. Wird immer mit DT_SET_IMMEDIATE verwendet.
    
Diese Eigenschaft wird im ulCtlFlags-Element der [DTCTL](dtctl.md) -Struktur eines Steuerelements gespeichert. Die meisten der Steuerelement-Flags gelten für alle Steuerelemente, die Benutzereingaben zulassen; einige wenige gelten nur für das Bearbeitungssteuerelement. Steuerelemente, die keine Benutzereingabe zulassen, beispielsweise eine Schaltfläche oder eine Bezeichnung, legen 0 für Ihre Steuerelement-Flags fest. 
  
Viele der Flags-Werte sind selbsterklärend. Wenn DT_REQUIRED beispielsweise für ein Steuerelement festgelegt ist, muss es einen Wert enthalten, bevor das Dialogfeld geschlossen werden kann. Entweder kann der Dienstanbieter einen Wert über die **IMAPIProp** -Implementierung angeben, oder der Benutzer kann eine eingeben. DT_EDITABLE gibt an, dass der Wert für das Steuerelement geändert werden kann. DT_MULTILINE ermöglicht, dass der Wert für ein Bearbeitungssteuerelement mehrere Zeilen umfasst. 
  
Einige Steuerelement-Flags sind nicht so offensichtlich. Wenn ein Steuerelement das DT_SET_IMMEDIATE-Flag festlegt, wirken sich Änderungen an seinem Wert ab, sobald der Benutzer zu einem neuen Steuerelement wechselt. MAPI führt einen einzelnen Aufruf der [IMAPIProp::](imapiprop-setprops.md) SetProps-Methode der Property-Schnittstelle für die Eigenschaft des Steuerelements aus. Dies unterscheidet sich vom Standardverhalten, das bedeutet, dass Änderungen an den Steuerelementwerten erst wirksam werden, wenn der Benutzer die Schaltfläche **OK** auswählt oder das Dialogfeld abschließt. Das DT_SET_IMMEDIATE-Flag wird häufig in Kombination mit Anzeige Tabellen Benachrichtigungen verwendet. 
  
In der folgenden Tabelle werden die Typen von Steuerelementen und alle Flagwerte aufgelistet, die für jeden Typ festgelegt werden können.
  
|**Control**|**Gültige Werte für diese Eigenschaft**|
|:-----|:-----|
|Schaltfläche  <br/> |Muss NULL sein  <br/> |
|Kontrollkästchen  <br/> |DT_EDITABLE, DT_SET_IMMEDIATE  <br/> |
|Kombinationsfeld  <br/> |DT_EDITABLE, DT_REQUIRED, DT_SET_IMMEDIATE  <br/> |
|Dropdown-Listenfeld  <br/> |DT_EDITABLE, DT_SET_IMMEDIATE  <br/> |
|Bearbeiten  <br/> |DT_ACCEPT_DBCS, DT_MULTILINE, DT_EDITABLE, DT_PASSWORD_EDIT, DT_REQUIRED, DT_SET_IMMEDIATE  <br/> |
|Gruppenfeld  <br/> |Muss NULL sein  <br/> |
|Label  <br/> |Muss NULL sein  <br/> |
|Listenfeld  <br/> |Muss NULL sein  <br/> |
|MehrWertiges Dropdown-Listenfeld  <br/> |Muss NULL sein  <br/> |
|MehrWertiges Listenfeld  <br/> |Muss NULL sein  <br/> |
|Registerkartenseite  <br/> |Muss NULL sein  <br/> |
|Optionsfeld  <br/> |Muss NULL sein  <br/> |
   
## <a name="related-resources"></a>Zugehörige Ressourcen

### <a name="header-files"></a>Header Dateien

Mapidefs. h
  
> Stellt Datentypdefinitionen bereit.
    
Mapitags. h
  
> Enthält Definitionen von Eigenschaften, die als Alternative Namen aufgeführt sind.
    
## <a name="see-also"></a>Siehe auch



[MAPI-Eigenschaften](mapi-properties.md)
  
[Kanonische MAPI-Eigenschaften](mapi-canonical-properties.md)
  
[Zuordnen von kanonischen Eigenschaftennamen zu MAPI-Namen](mapping-canonical-property-names-to-mapi-names.md)
  
[Zuordnen von MAPI-Namen zu kanonischen Eigenschaftennamen](mapping-mapi-names-to-canonical-property-names.md)

