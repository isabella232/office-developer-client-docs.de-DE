---
title: Anzeigen von Tabellen
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.localizationpriority: medium
api_type:
- COM
ms.assetid: c314ff6d-3e60-4b81-87ac-6ca6753ff633
description: 'Letzte Änderung: Montag, 9. März 2015'
ms.openlocfilehash: fa65f150639a0604ee84f038c92cec0b0a10e43e
ms.sourcegitcommit: a1d9041c20256616c9c183f7d1049142a7ac6991
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 09/24/2021
ms.locfileid: "59588171"
---
# <a name="display-tables"></a>Anzeigen von Tabellen

  
  
**Gilt für**: Outlook 2013 | Outlook 2016 
  
In einer Anzeigetabelle wird beschrieben, wie ein bestimmter Dialogfeldtyp angezeigt wird– eine oder mehrere Eigenschaftenseiten mit Registerkarten, die für das Anzeigen und möglicherweise Bearbeiten einer oder mehrerer Eigenschaften vorgesehen sind. Jeder Anzeigetabelle ist eine [IMAPIProp zugeordnet: IUnknown-Schnittstellenimplementierungen.](imapipropiunknown.md) Die **IMAPIProp-Implementierung** verwaltet die Eigenschaftendaten, die im Dialogfeld angezeigt werden. 
  
Die Zeilen in einer Anzeigetabelle stellen die Steuerelemente oder Benutzeroberflächenobjekte dar, die im Dialogfeld angezeigt werden. MAPI definiert viele Arten von Steuerelementen, einige mit statischen Werten und einige mit dynamischen Werten, die ein Benutzer ändern kann. Die meisten Steuerelemente können Eigenschaften zugeordnet werden, die mit der **IMAPIProp-Implementierung** verwaltet werden. Wenn ein Benutzer den Wert eines modifizierbaren Steuerelements ändert, wird die entsprechende Eigenschaft aktualisiert. 
  
Dienstanbieter implementieren Anzeigetabellen und die **IMAPIProp-Schnittstelle.** Das Erstellen einer Anzeigetabelle ähnelt dem Schreiben eines Programms mit einer Skriptsprache. Dienstanbieter können eine Anzeigetabelle erstellen, indem sie: 
  
- Aufrufen der [BuildDisplayTable-Funktion.](builddisplaytable.md) 
    
    - Oder -
    
- Einschließen von benutzerdefiniertem Code, der die Anzeigetabelle direkt mithilfe eines Tabellendatenobjekts auffüllt – ein Objekt, das die [ITableData : IUnknown-Schnittstelle](itabledataiunknown.md) unterstützt. 
    
Die **BuildDisplayTable-Funktion** kombiniert Informationen aus Anzeigetabellenstrukturen mit visuellen Elementen aus einer Dialogfeldressource, um Anzeigetabellenzeilen zu erstellen. Die Funktion gibt einen Zeiger auf eine [IMAPITable zurück: IUnknown-Schnittstellenimplementierung](imapitableiunknown.md) und, falls angefordert, einen Zeiger auf eine ITableData-Schnittstellenimplementierung.  
  
Die Verwendung von **BuildDisplayTable** zum Erstellen einer Anzeigetabelle ist einfach und erleichtert die Wartung, wenn sich visuelle Elemente der Anzeige ändern. Dienstanbieter, die keine **BuildDisplayTable** verwenden möchten, können jedoch eine Anzeigetabelle mit benutzerdefiniertem Code erstellen, der die Methoden von **ITableData** verwendet. Beispielsweise möchten Dienstanbieter, die über eine vorhandene Vorlagenstruktur für ihre Eigenschaftenseiten verfügen, möglicherweise benutzerdefinierten Code erstellen, anstatt **BuildDisplayTable** zu verwenden.
  
Es gibt eine Vielzahl von Möglichkeiten, wie Dienstanbieter die Eigenschaftenschnittstelle für ihre Anzeigetabelle implementieren können. Zu diesen zählen:
  
- Bereitstellen einer standardmäßigen [IMAPIProp: IUnknown-Implementierung.](imapipropiunknown.md) 
    
- Bereitstellen einer umschlossenen **IMAPIProp-Implementierung,** die eine spezielle Verarbeitung umfasst, bevor die Standardaufrufe ausgeführt werden. 
    
- Bereitstellen einer [IPropData: IMAPIProp-Implementierung.](ipropdataimapiprop.md) 
    
Die Art der Implementierung hängt von den Merkmalen der anzuzeigenden Daten und dem verantwortlichen Dienstanbieter ab. Wenn beispielsweise eine implizite Beziehung zwischen den Daten in zwei Bearbeitungssteuerelementen besteht und eines der Steuerelemente geändert wird, muss die **IMAPIProp-Implementierung** den Wert des anderen Steuerelements entsprechend ändern. 
  
Anzeigetabellen verfügen über die folgenden Eigenschaften im erforderlichen Spaltensatz:
  
|||
|:-----|:-----|
|**PR_XPOS** ([PidTagXCoordinate](pidtagxcoordinate-canonical-property.md))  <br/> |**PR_YPOS** ([PidTagYCoordinate](pidtagycoordinate-canonical-property.md))  <br/> |
|**PR_DELTAX** ([PidTagDeltaX](pidtagdeltax-canonical-property.md))  <br/> |**PR_DELTAY** ([PidTagDeltaY](pidtagdeltay-canonical-property.md))  <br/> |
|**PR_CONTROL_TYPE** ([PidTagControlType](pidtagcontroltype-canonical-property.md))  <br/> |**PR_CONTROL_FLAGS** ([PidTagControlFlags](pidtagcontrolflags-canonical-property.md))  <br/> |
|**PR_CONTROL_STRUCTURE** ([PidTagControlStructure](pidtagcontrolstructure-canonical-property.md))  <br/> |**PR_CONTROL_ID** ([PidTagControlId](pidtagcontrolid-canonical-property.md))  <br/> |
   
 **PR_XPOS** und **PR_YPOS** die X- und Y-Koordinaten der oberen linken Ecke des Steuerelements angeben. Die horizontalen Einheiten sind 1/4 der Basisbreiteneinheit des Dialogfelds. Die vertikalen Einheiten sind 1/8 der Basishöheneinheit des Dialogfelds. Windows berechnet die basiseinheiten des aktuellen Dialogfelds aus der Höhe und Breite der aktuellen Systemschriftart. Die Koordinaten sind relativ zum Ursprung des Eigenschaftenseitenbereichs. Die Größe von Eigenschaftenseiten ist auf ca. 200 x 180 Dialogfeldeinheiten beschränkt. 
  
 **PR_DELTAX** und **PR_DELTAY** sind die Breite und Höhe des Steuerelements. Dies sind ULONG-Werte. Die Breiteneinheiten sind 1/4 der Basisbreiteneinheit des Dialogfelds. Die Höheneinheiten sind 1/8 der Basishöheneinheit des Dialogfelds. Die Koordinaten sind relativ zum Ursprung des Steuerelements. 
  
Die anderen vier Eigenschaften beschreiben verschiedene Merkmale des Steuerelements. **PR_CONTROL_TYPE** gibt den Typ des Steuerelements an. MAPI definiert zwölf Arten von Steuerelementen mit jeweils unterschiedlichen Attributen. Diese Attribute werden in der Flags-Eigenschaft **PR_CONTROL_FLAGS** beschrieben. Beispiele für Attribute sind, ob ein Steuerelement bearbeitbar oder erforderlich ist. 
  
Die Steuerelementstruktur **PR_CONTROL_STRUCTURE** enthält Informationen, die für den jeweiligen Steuerelementtyp relevant sind. Jeder Steuerelementtyp wird mit einer anderen Struktur beschrieben. Bearbeitungssteuerelemente werden beispielsweise mit der [DTBLEDIT-Struktur](dtbledit.md) beschrieben. **DTBLEDIT-Strukturen** enthalten Elemente, die die Anzahl und bestimmte Typen von Zeichen auflisten, die auf dem Steuerelement platziert werden können, sowie ein Eigenschaftstag, das die Eigenschaft identifiziert, deren Wert im Steuerelement angezeigt werden soll. **PR_CONTROL_STRUCTURE** wird als binäre Eigenschaft gespeichert. 
  
Der Steuerelementbezeichner, **PR_CONTROL_ID,** identifiziert das Steuerelement eindeutig im dialogfeld, das von der Anzeigetabelle beschrieben wird. **PR_CONTROL_ID** wird aus den Werten festgelegt, die in den  *LpbNotif-*  und  *cbNotif-Elementen*  der [DTCTL-Struktur](dtctl.md) platziert werden, die von **BuildDisplayTable** zum Erstellen der Anzeigetabelle verwendet wird. Da MAPI manchmal Anzeigetabellen kombiniert, sollte der Bezeichner in **PR_CONTROL_ID** immer eindeutig sein. In der Regel weisen Anbieter **PR_CONTROL_ID** eine [GUID-Struktur](guid.md) zu, um ihre Eindeutigkeit sicherzustellen. Die **PR_CONTROL_ID-Eigenschaft** ist in der [TABLE_NOTIFICATION](table_notification.md) Struktur enthalten, wenn eine Anzeigetabellenbenachrichtigung generiert wird. 
  
Weitere Informationen zu Anzeigetabellen finden Sie unter [Display Table Implementation](display-table-implementation.md) und About Display Table [Notifications](about-display-table-notifications.md). 
  
## <a name="see-also"></a>Siehe auch



[MAPI-Tabellen](mapi-tables.md)

