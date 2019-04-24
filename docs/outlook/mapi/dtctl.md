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
description: 'Letzte �nderung: Montag, 9. M�rz 2015'
ms.openlocfilehash: 2a2ca1fba5dceb45b41c2f25a96e163f02c41440
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 04/23/2019
ms.locfileid: "32339410"
---
# <a name="dtctl"></a>DTCTL

**Gilt für**: Outlook 2013 | Outlook 2016 
  
Beschreibt ein Steuerelement, das in einem von einer Anzeigetabelle erstellten Dialogfeldverwendet wird. 
  
|||
|:-----|:-----|
|Headerdatei  <br/> |Mapidefs. h  <br/> |
   
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
  
> Der Typ des Steuerelements, das im **CTL** -Element enthalten ist und der **PR_CONTROL_TYPE** ([pidtagcontroltype (](pidtagcontroltype-canonical-property.md))-Eigenschaft des Steuerelements entspricht. Folgende Werte sind möglich:
    
DTCT_LABEL 
  
> Bezeichnungsfeld-Steuerelement.
    
DTCT_EDIT 
  
> Bearbeitungssteuerelement.
    
DTCT_LBX 
  
> Listenfeld-Steuerelement.
    
DTCT_COMBOBOX 
  
> Kombinationsfeld-Steuerelement.
    
DTCT_DDLBX 
  
> Dropdownlisten-Steuerelement.
    
DTCT_CHECKBOX 
  
> Kontrollkästchen-Steuerelement.
    
DTCT_GROUPBOX 
  
> Gruppenfeld-Steuerelement.
    
DTCT_BUTTON 
  
> Schaltflächen-Steuerelement.
    
DTCT_PAGE 
  
> Seitensteuerelement mit Registerkarten.
    
DTCT_RADIOBUTTON 
  
> Optionsfeld-Steuerelement.
    
DTCT_MVLISTBOX 
  
> Mehrwertiges Listensteuerelement.
    
DTCT_MVDDLBX 
  
> Dropdownlisten-Steuerelement mit mehreren Werten.
    
**ulCtlFlags**
  
> Bitmaske von Flags, die die Features des Steuerelements beschreibt und der **PR_CONTROL_FLAGS** ([pidtagcontrolflags (](pidtagcontrolflags-canonical-property.md))-Eigenschaft des Steuerelements entspricht. Diese Flags können nur für Kontrollkästchen, Kombinationsfelder, Listenfelder und Bearbeitungssteuerelemente festgelegt werden. Folgende Werte sind möglich:
    
DT_ACCEPT_DBCS 
  
> Das ANSI-oder das DBCS-Format wird akzeptiert. Dieses Flag ist nur für Bearbeitungssteuerelemente gültig.
    
DT_EDITABLE 
  
> Ein Benutzer kann den Text im Steuerelement ändern. 
    
DT_MULTILINE 
  
> Das Steuerelement kann mehrere Textzeilen enthalten. Dieses Flag ist nur für Bearbeitungssteuerelemente gültig.
    
DT_PASSWORD_EDIT 
  
> Das Steuerelement enthält ein Kennwort; Daher sollte dem Benutzer der Inhalt des Steuerelements nicht angezeigt werden. Dieses Flag ist nur für Bearbeitungssteuerelemente gültig.
    
DT_REQUIRED 
  
> Das Dialogfeld-Steuerelement ist erforderlich. Dieses Flag ist nur für Bearbeitungs-und Kombinationsfeld-Steuerelemente gültig.
    
DT_SET_IMMEDIATE 
  
> Ermöglicht die sofortige Ausgabe eines Werts bei einer Änderung im Steuerelement. Dadurch kann eine Abhängigkeitsbeziehung zwischen zwei Steuerelementen hergestellt werden. 
    
**lpbNotif**
  
> Zeiger auf eine Struktur, die aus einer [GUID](guid.md) -Struktur besteht, die den Dienstanbieter und einen Bezeichner für das Steuerelement darstellt. Die **lpbNotif** -und **cbNotif** -Member entsprechen der **PR_CONTROL_ID** ([pidtagcontrolid (](pidtagcontrolid-canonical-property.md))-Eigenschaft des Steuerelements und werden verwendet, um die Benutzeroberfläche zu benachrichtigen, wenn das Steuerelement aktualisiert werden muss.
    
**cbNotif**
  
> Die Anzahl der Bytes in der Struktur, auf die durch das **lpbNotif** -Element verwiesen wird. 
    
**lpszFilter**
  
> Zeiger auf eine Zeichenfolge, die beschreibt, welche Zeichen in ein Bearbeitungs-oder Kombinationsfeld-Steuerelement eingegeben werden können. Bei anderen Steuerelementtypen kann das **lpszFilter** -Element NULL sein. Bei Bearbeitungs-und Kombinationsfeld-Steuerelementen sollte es sich um einen regulären Ausdruck handeln, der jeweils auf ein einzelnes Zeichen angewendet wird. Derselbe Filter wird auf alle Zeichen im Steuerelement angewendet. Das Format der Filterzeichenfolge lautet wie folgt: 
    
|**Zeichen**|**Beschreibung**|
|:-----|:-----|
| `*` <br/> | Ein beliebiges Zeichen ist zulässig (Beispiels `"*"`Weise).  <br/> |
| `[ ]` <br/> |Definiert eine Gruppe von Zeichen (beispielsweise `"[0123456789]"`.)  <br/> |
| `-` <br/> |Gibt einen Zeichentyp an (beispielsweise `"[a-z]"`).  <br/> |
| `~` <br/> |Gibt an, dass diese Zeichen nicht zulässig sind (zum `"[~0-9]")`Beispiel. <br/>|   
| `\` <br/> |Wird verwendet, um eines der vorherigen Symbole zu zitieren ( `"[\-\\\[\]]"` beispielsweise sind \, means-, [und] characters zulässig).  <br/> |
   
**ulItemID**
  
> Wert, der das Steuerelement in der Dialogfeldressource identifiziert. Bei Registerkarten-Steuerelementen vom Typ DTCT_PAGE wird optional das **ulItemID** -Element verwendet, um den Komponentennamen für die Seite aus einer String-Ressource zu laden. Positions-und Beschriftungsinformationen werden aus der Dialogfeldressource gelesen. 
    
**veraltete**
  
> Eine Struktur, die die Daten für das Steuerelement enthält und der **PR_CONTROL_STRUCTURE** ([pidtagcontrolstructure (](pidtagcontrolstructure-canonical-property.md))-Eigenschaft des Steuerelements entspricht. Jeder Steuerelementtyp hat eine andere Struktur.
    
## <a name="remarks"></a>Bemerkungen

Die **DTCTL** -Struktur beschreibt ein Steuerelement eines beliebigen Typs. Die meisten seiner Member werden verwendet, um Eigenschaften für das Steuerelement festzulegen. 
  
Der **CTL** -Member ist eine Vereinigung von Strukturen, die sich auf einen bestimmten Steuerelementtyp beziehen. Wenn die **DTCTL** -Struktur ein Edit-Steuerelement beschreibt, zeigt der **CTL** -Member beispielsweise auf eine [DTBLEDIT](dtbledit.md) -Struktur. Diese Struktur entspricht der **PR_CONTROL_STRUCTURE** -Eigenschaft des Steuerelements. Die Union hat als erster Member eine Variable vom Typ LPVOID, um die Kompilierungszeit Initialisierung der **DTCTL** -Struktur zu ermöglichen. 
  
Obwohl die [BuildDisplayTable](builddisplaytable.md) -Funktion die **DTCTL** -Struktur zum Erstellen der Anzeigetabelle aus den Steuerelementressourcen verwendet, wird die **DTCTL** -Struktur nie in der Anzeigetabelle selbst angezeigt. Diese Struktur liefert nur Informationen an **BuildDisplayTable**.
  
Im **ulCtlFlags** -Element betreffen vier Flags DT_ACCEPT_DBCS, DT_EDITABLE, DT_MULTILINE_and DT_PASSWORD_EDIT nur Bearbeitungssteuerelemente. Zwei weitere DT_REQUIRED und DT_SET_IMMEDIATE wirken sich auf ein bearbeitbares Steuerelement aus. 
  
Zu den verfügbaren Steuerelementen für ein Dialogfeld gehören die Bezeichnungen, das Textfeld, das Textfeld, die Liste, die Dropdownliste, das Kombinationsfeld, das Kontrollkästchen, das Gruppenfeld, die Schaltfläche, die Optionsschaltfläche und die Registerkartenseite.
  
Eine Übersicht über Anzeige Tabellen finden Sie unter [Display Tables](display-tables.md). Weitere Informationen zum Implementieren einer Anzeigetabelle finden Sie unter [Implementieren einer Anzeigetabelle](display-table-implementation.md).
  
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

