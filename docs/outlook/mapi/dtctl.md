---
title: DTCTL
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- MAPI.DTCTL
api_type:
- COM
ms.assetid: 6d1589e9-b171-427a-9a3e-b4154ee8ceb6
description: 'Letzte Änderung: Montag, 9. März 2015'
ms.openlocfilehash: 2a2ca1fba5dceb45b41c2f25a96e163f02c41440
ms.sourcegitcommit: 8657170d071f9bcf680aba50b9c07f2a4fb82283
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 04/28/2019
ms.locfileid: "33421501"
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

## <a name="members"></a>Elemente

**ulCtlType**
  
> Typ des Steuerelements, das im **#A0** enthalten ist und der PR_CONTROL_TYPE **(** [PidTagControlType](pidtagcontroltype-canonical-property.md)) des Steuerelements entspricht. Mögliche Werte sind:
    
DTCT_LABEL 
  
> Bezeichnungsfeld-Steuerelement.
    
DTCT_EDIT 
  
> Steuerelement bearbeiten.
    
DTCT_LBX 
  
> Listenfeldsteuerelement.
    
DTCT_COMBOBOX 
  
> Kombinationsfeldsteuerelement.
    
DTCT_DDLBX 
  
> Dropdownlistensteuerelement.
    
DTCT_CHECKBOX 
  
> Kontrollkästchen-Steuerelement.
    
DTCT_GROUPBOX 
  
> Gruppenfeldsteuerelement.
    
DTCT_BUTTON 
  
> Schaltflächensteuerelement.
    
DTCT_PAGE 
  
> Seitensteuerelement mit Registerkarten.
    
DTCT_RADIOBUTTON 
  
> Optionsfeldsteuerelement.
    
DTCT_MVLISTBOX 
  
> Mehrwertiges Listensteuerelement.
    
DTCT_MVDDLBX 
  
> Mehrwertige Dropdownlistensteuerung.
    
**ulCtlFlags**
  
> Bitmaske von Flags, die die Features des Steuerelements beschreibt und der **PR_CONTROL_FLAGS** ([PidTagControlFlags](pidtagcontrolflags-canonical-property.md)) -Eigenschaft des Steuerelements entspricht. Diese Kennzeichen können nur für Kontrollkästchen, Kombinationsfelder, Listenfelder und Bearbeitungssteuerelemente festgelegt werden. Mögliche Werte sind:
    
DT_ACCEPT_DBCS 
  
> Entweder das ANSI- oder das DBCS-Format wird akzeptiert. Dieses Flag ist nur für Bearbeitungssteuerelemente gültig.
    
DT_EDITABLE 
  
> Ein Benutzer kann den Text im Steuerelement ändern. 
    
DT_MULTILINE 
  
> Das Steuerelement kann mehrere Textzeilen enthalten. Dieses Flag ist nur für Bearbeitungssteuerelemente gültig.
    
DT_PASSWORD_EDIT 
  
> Das Steuerelement enthält ein Kennwort. Daher sollte der Inhalt des Steuerelements dem Benutzer nicht angezeigt werden. Dieses Flag ist nur für Bearbeitungssteuerelemente gültig.
    
DT_REQUIRED 
  
> Das Dialogfeldsteuerelement ist erforderlich. Dieses Flag ist nur für Bearbeitungs- und Kombinationsfeldsteuerelemente gültig.
    
DT_SET_IMMEDIATE 
  
> Ermöglicht die sofortige Ausgabe eines Werts bei einer Änderung im Steuerelement. Dadurch kann eine Abhängigkeitsbeziehung zwischen zwei Steuerelementen hergestellt werden. 
    
**lpbNotif**
  
> Zeiger auf eine Struktur, die aus einer [GUID-Struktur](guid.md) besteht, um den Dienstanbieter und einen Bezeichner für das Steuerelement zu repräsentieren. Die **Elemente lpbNotif** und **cbNotif** entsprechen der **PR_CONTROL_ID** ([PidTagControlId](pidtagcontrolid-canonical-property.md))-Eigenschaft des Steuerelements und werden verwendet, um die Benutzeroberfläche zu benachrichtigen, wenn das Steuerelement aktualisiert werden muss.
    
**cbNotif**
  
> Anzahl der Bytes in der Struktur, auf die das **lpbNotif-Element** verweist. 
    
**lpszFilter**
  
> Zeiger auf eine Zeichenzeichenfolge, die beschreibt, welche Zeichen in ein Bearbeitungs- oder Kombinationsfeldsteuerelement eingegeben werden können. Bei anderen Steuerelementtypen kann **das lpszFilter-Element** NULL sein. Für Bearbeitungs- und Kombinationsfeldsteuerelemente sollte es sich um einen regulären Ausdruck, der für ein einzelnes Zeichen gleichzeitig gilt, sein. Der gleiche Filter wird auf alle Zeichen im Steuerelement angewendet. Das Format der Filterzeichenfolge lautet wie folgt: 
    
|**Zeichen**|**Beschreibung**|
|:-----|:-----|
| `*` <br/> | Jedes Zeichen ist zulässig (z. B. `"*"` ).  <br/> |
| `[ ]` <br/> |Definiert eine Reihe von Zeichen (z. B. `"[0123456789]"` .)  <br/> |
| `-` <br/> |Gibt einen Zeichenbereich an (z. B. `"[a-z]"` ).  <br/> |
| `~` <br/> |Gibt an, dass diese Zeichen nicht zulässig sind (z. B. `"[~0-9]")` . <br/>|   
| `\` <br/> |Wird verwendet, um eines der vorherigen Symbole anführungszeichen (z. B. `"[\-\\\[\]]"` bedeutet -, \, [und ] Zeichen sind zulässig).  <br/> |
   
**ulItemID**
  
> Wert, der das Steuerelement in der Dialogfeldressource identifiziert. Bei Registerkartenseitensteuerelementen vom Typ DTCT_PAGE wird das **ulItemID-Element** optional zum Laden des Komponentennamens für die Seite aus einer Zeichenfolgenressource verwendet. Positions- und Bezeichnungsinformationen werden aus der Dialogfeldressource gelesen. 
    
**ctl**
  
> Eine Struktur, die die Daten für das Steuerelement enthält und der PR_CONTROL_STRUCTURE **(** [PidTagControlStructure](pidtagcontrolstructure-canonical-property.md)) des Steuerelements entspricht. Jeder Steuerelementtyp hat eine andere Struktur.
    
## <a name="remarks"></a>Hinweise

Die **DTCTL-Struktur** beschreibt ein Steuerelement eines beliebigen Typs. Die meisten Elemente werden zum Festlegen von Eigenschaften für das Steuerelement verwendet. 
  
Das **#A0** ist eine Vereinigung von Strukturen, die sich auf einen bestimmten Steuerelementtyp beziehen. Wenn die **DTCTL-Struktur** beispielsweise ein Bearbeitungssteuerelement beschreibt, zeigt das **#A0** auf eine [DTBLEDIT-Struktur.](dtbledit.md) Diese Struktur entspricht der  PR_CONTROL_STRUCTURE Steuerelements. Die Union verfügt als erstes Mitglied über eine Variable vom Typ LPVOID, um die Initialisierung der Kompilierungszeit der **DTCTL-Struktur zu** ermöglichen. 
  
Obwohl die [BuildDisplayTable-Funktion](builddisplaytable.md) die **DTCTL-Struktur** zum Erstellen der Anzeigetabelle aus Steuerelementressourcen verwendet, wird die **DTCTL-Struktur** niemals in der Anzeigetabelle selbst angezeigt. Diese Struktur stellt nur Informationen für **BuildDisplayTable zur Verfügung.**
  
Im **ulCtlFlags-Element** werden vier Flags DT_ACCEPT_DBCS, DT_EDITABLE, DT_MULTILINE_and DT_PASSWORD_EDIT nur Bearbeitungssteuerelemente betreffen. Zwei weitere DT_REQUIRED und DT_SET_IMMEDIATE sich auf ein bearbeitbares Steuerelement. 
  
Die für ein Dialogfeld verfügbaren Steuerelemente sind Bezeichnung, Textfeld, Freihandtextfeld, Liste, Dropdownliste, Kombinationsfeld, Kontrollkästchen, Gruppenfeld, Schaltfläche, Optionsfeld und Registerkartenseite.
  
Eine Übersicht über Anzeigetabellen finden Sie unter [Display Tables](display-tables.md). Informationen zum Implementieren einer Anzeigetabelle finden Sie unter [Implementieren einer Anzeigetabelle](display-table-implementation.md).
  
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

