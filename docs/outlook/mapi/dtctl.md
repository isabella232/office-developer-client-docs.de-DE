---
title: DTCTL
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
ms.localizationpriority: medium
api_name:
- MAPI.DTCTL
api_type:
- COM
ms.assetid: 6d1589e9-b171-427a-9a3e-b4154ee8ceb6
description: 'Letzte Änderung: Montag, 9. März 2015'
ms.openlocfilehash: d0321019c383994fa51f9d205504a0636e2c973b
ms.sourcegitcommit: a1d9041c20256616c9c183f7d1049142a7ac6991
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 09/24/2021
ms.locfileid: "59567704"
---
# <a name="dtctl"></a>DTCTL

**Gilt für**: Outlook 2013 | Outlook 2016 
  
Beschreibt ein Steuerelement, das in einem Dialogfeld verwendet wird, das aus einer Anzeigetabelle erstellt wird. 
  
|||
|:-----|:-----|
|Headerdatei  <br/> |Mapidefs.h  <br/> |
   
```cpp
typedef struct
{
  ULONG ulCtlType;
  ULONG ulCtlFlags;
  LPBYTE lpbNotif;
  ULONG cbNotif;
  LPSTR lpszFilter;
  ULONG ulItemID;
  union
  {
    LPVOID lpv;
    LPDTBLLABEL lplabel;
    LPDTBLEDIT lpedit;
    LPDTBLLBX lplbx;
    LPDTBLCOMBOBOX lpcombobox;
    LPDTBLDDLBX lpddlbx;
    LPDTBLCHECKBOX lpcheckbox;
    LPDTBLGROUPBOX lpgroupbox;
    LPDTBLBUTTON lpbutton;
    LPDTBLRADIOBUTTON lpradiobutton;
    LPDTBLMVLISTBOX lpmvlbx;
    LPDTBLMVDDLBX lpmvddlbx;
    LPDTBLPAGE lppage;
  } ctl;
} DTCTL, FAR *LPDTCTL;

```

## <a name="members"></a>Members

**ulCtlType**
  
> Typ des Steuerelements, das im **ctl-Element** enthalten ist und der **PR_CONTROL_TYPE** ([PidTagControlType](pidtagcontroltype-canonical-property.md)) -Eigenschaft des Steuerelements entspricht. Mögliche Werte sind:
    
DTCT_LABEL 
  
> Bezeichnungsfeld-Steuerelement.
    
DTCT_EDIT 
  
> Bearbeitungssteuerelement.
    
DTCT_LBX 
  
> Listenfeld-Steuerelement.
    
DTCT_COMBOBOX 
  
> Kombinationsfeld-Steuerelement.
    
DTCT_DDLBX 
  
> Dropdownlistensteuerelement.
    
DTCT_CHECKBOX 
  
> Kontrollkästchen-Steuerelement.
    
DTCT_GROUPBOX 
  
> Gruppenfeld-Steuerelement.
    
DTCT_BUTTON 
  
> Schaltflächensteuerelement.
    
DTCT_PAGE 
  
> Steuerelement für Registerkartenseite.
    
DTCT_RADIOBUTTON 
  
> Optionsfeld-Steuerelement.
    
DTCT_MVLISTBOX 
  
> Mehrwertiges Listensteuerelement.
    
DTCT_MVDDLBX 
  
> Mehrwertiges Dropdownlistensteuerelement.
    
**ulCtlFlags**
  
> Bitmaske von Flags, die die Features des Steuerelements beschreibt und der **PR_CONTROL_FLAGS** ([PidTagControlFlags](pidtagcontrolflags-canonical-property.md)) -Eigenschaft des Steuerelements entspricht. Diese Flags können nur für Kontrollkästchen, Kombinationsfelder, Listenfelder und Bearbeitungssteuerelemente festgelegt werden. Mögliche Werte sind:
    
DT_ACCEPT_DBCS 
  
> Das ANSI- oder DBCS-Format wird akzeptiert. Dieses Kennzeichen ist nur für Bearbeitungssteuerelemente gültig.
    
DT_EDITABLE 
  
> Ein Benutzer kann den Text im Steuerelement ändern. 
    
DT_MULTILINE 
  
> Das Steuerelement kann mehrere Textzeilen enthalten. Dieses Kennzeichen ist nur für Bearbeitungssteuerelemente gültig.
    
DT_PASSWORD_EDIT 
  
> Das Steuerelement enthält ein Kennwort. daher sollte der Inhalt des Steuerelements dem Benutzer nicht angezeigt werden. Dieses Kennzeichen ist nur für Bearbeitungssteuerelemente gültig.
    
DT_REQUIRED 
  
> Das Dialogfeld-Steuerelement ist erforderlich. Dieses Kennzeichen gilt nur für Bearbeitungs- und Kombinationsfeld-Steuerelemente.
    
DT_SET_IMMEDIATE 
  
> Aktiviert die sofortige Ausgabe eines Werts bei einer Änderung des Steuerelements. Dadurch kann eine Abhängigkeitsbeziehung zwischen zwei Steuerelementen hergestellt werden. 
    
**lpbNotif**
  
> Zeiger auf eine Struktur, die aus einer [GUID-Struktur](guid.md) besteht, um den Dienstanbieter und einen Bezeichner für das Steuerelement darzustellen. Die **Elemente lpbNotif** und **cbNotif** entsprechen der **Eigenschaft PR_CONTROL_ID** ([PidTagControlId](pidtagcontrolid-canonical-property.md)) des Steuerelements und werden verwendet, um die Benutzeroberfläche zu benachrichtigen, wenn das Steuerelement aktualisiert werden muss.
    
**cbNotif**
  
> Anzahl der Bytes in der Struktur, auf die der **lpbNotif-Member** verweist. 
    
**lpszFilter**
  
> Zeiger auf eine Zeichenfolge, die beschreibt, welche Zeichen in ein Bearbeitungs- oder Kombinationsfeld-Steuerelement eingegeben werden können. Bei anderen Steuerelementtypen kann der **lpszFilter-Member** NULL sein. Bei Bearbeitungs- und Kombinationsfeld-Steuerelementen sollte es sich um einen regulären Ausdruck handelt, der jeweils für ein einzelnes Zeichen gilt. Derselbe Filter wird auf alle Zeichen im Steuerelement angewendet. Das Format der Filterzeichenfolge lautet wie folgt: 
    
|**Zeichen**|**Beschreibung**|
|:-----|:-----|
| `*` <br/> | Ein beliebiges Zeichen ist zulässig (z. B. `"*"` ).  <br/> |
| `[ ]` <br/> |Definiert einen Satz von Zeichen (z. B. `"[0123456789]"` .)  <br/> |
| `-` <br/> |Gibt einen Bereich von Zeichen an (z. B. `"[a-z]"` ).  <br/> |
| `~` <br/> |Gibt an, dass diese Zeichen nicht zulässig sind `"[~0-9]")` (z. B. . <br/>|   
| `\` <br/> |Wird verwendet, um eines der vorherigen Symbole anführungszeichen (z. B. `"[\-\\\[\]]"` "-"-" \, [und "]"-Zeichen sind zulässig).  <br/> |
   
**ulItemID**
  
> Wert, der das Steuerelement in der Dialogfeldressource identifiziert. Für Steuerelemente mit Registerkartenseiten vom Typ DTCT_PAGE das **ulItemID-Element** optional verwendet wird, um den Komponentennamen für die Seite aus einer Zeichenfolgenressource zu laden. Positions- und Bezeichnungsinformationen werden aus der Dialogfeldressource gelesen. 
    
**Ctl**
  
> Eine Struktur, die die Daten für das Steuerelement enthält und der **PR_CONTROL_STRUCTURE** ([PidTagControlStructure](pidtagcontrolstructure-canonical-property.md)) -Eigenschaft des Steuerelements entspricht. Jeder Steuerelementtyp weist eine andere Struktur auf.
    
## <a name="remarks"></a>HinwBemerkungeneise

Die **DTCTL-Struktur** beschreibt ein Steuerelement eines beliebigen Typs. Die meisten Seiner Member werden verwendet, um Eigenschaften für das Steuerelement festzulegen. 
  
Das **ctl-Element** ist eine Vereinigung von Strukturen, die sich auf einen bestimmten Steuerelementtyp beziehen. Wenn die **DTCTL-Struktur** beispielsweise ein Bearbeitungssteuerelement beschreibt, verweist das **ctl-Element** auf eine [DTBLEDIT-Struktur.](dtbledit.md) Diese Struktur entspricht der **PR_CONTROL_STRUCTURE** Eigenschaft des Steuerelements. Die Vereinigung verfügt als erstes Mitglied über eine Variable vom Typ LPVOID, um die Initialisierung der **DTCTL-Struktur** zur Kompilierungszeit zu ermöglichen. 
  
Obwohl die [BuildDisplayTable-Funktion](builddisplaytable.md) die **DTCTL-Struktur** zum Erstellen der Anzeigetabelle aus Steuerelementressourcen verwendet, wird die **DTCTL-Struktur** nie in der Anzeigetabelle selbst angezeigt. Diese Struktur stellt lediglich Informationen für **BuildDisplayTable** bereit.
  
Im **ulCtlFlags-Element** wirken sich vier Flags DT_ACCEPT_DBCS, DT_EDITABLE, DT_MULTILINE_and DT_PASSWORD_EDIT nur auf Bearbeitungssteuerelemente aus. Zwei weitere DT_REQUIRED und DT_SET_IMMEDIATE sich auf jedes bearbeitbare Steuerelement auswirken. 
  
Die für ein Dialogfeld verfügbaren Steuerelemente sind Beschriftung, Textfeld, Freihandtextfeld, Liste, Dropdownliste, Kombinationsfeld, Kontrollkästchen, Gruppenfeld, Schaltfläche, Optionsfeld und Registerkartenseite.
  
Eine Übersicht über Anzeigetabellen finden Sie unter ["Anzeigetabellen".](display-tables.md) Informationen zum Implementieren einer Anzeigetabelle finden Sie unter [Implementieren einer Anzeigetabelle.](display-table-implementation.md)
  
## <a name="see-also"></a>Siehe auch

- [BuildDisplayTable](builddisplaytable.md)
- [DTBLBUTTON](dtblbutton.md)
- [DTBLCHECKBOX](dtblcheckbox.md)
- [DTBLCOMBOBOX](dtblcombobox.md)
- [DTBLDDLBX](dtblddlbx.md)
- [DTBLEDIT](dtbledit.md)
- [DTBLGROUPBOX](dtblgroupbox.md)
- [DTBLLABEL](dtbllabel.md)
- [DTBLLBX](dtbllbx.md)
- [DTBLMVDDLBOX](dtblmvddlbox.md)
- [DTBLMVLISTBOX](dtblmvlistbox.md)
- [DTBLPAGE](dtblpage.md)
- [DTBLRADIOBUTTON](dtblradiobutton.md)
- [MAPI-Strukturen](mapi-structures.md)

