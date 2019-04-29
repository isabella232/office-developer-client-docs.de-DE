---
title: Anzeige Tabellen
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
localization_priority: Normal
api_type:
- COM
ms.assetid: c314ff6d-3e60-4b81-87ac-6ca6753ff633
description: 'Letzte Änderung: Montag, 9. März 2015'
ms.openlocfilehash: 1b94b0ea69237be3675e1ea02fc3e2bfac337025
ms.sourcegitcommit: 8657170d071f9bcf680aba50b9c07f2a4fb82283
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 04/28/2019
ms.locfileid: "33406220"
---
# <a name="display-tables"></a>Anzeige Tabellen

  
  
**Gilt für**: Outlook 2013 | Outlook 2016 
  
In einer Anzeigetabelle wird beschrieben, wie ein bestimmter Dialogfeldtyp angezeigt wird: eine oder mehrere Registerkarten-Eigenschaftenseiten, die zum Anzeigen und Bearbeiten einer oder mehrerer Eigenschaften vorgesehen sind. Jeder Anzeigetabelle ist eine [IMAPIProp: IUnknown](imapipropiunknown.md) -Schnittstellenimplementierung zugeordnet. Die **IMAPIProp** -Implementierung verwaltet die Eigenschaftendaten, die im Dialogfeld angezeigt werden. 
  
Die Zeilen in einer Anzeigetabelle stellen die Steuerelemente oder Benutzeroberflächenobjekte dar, die im Dialogfeld angezeigt werden. MAPI definiert viele Typen von Steuerelementen, einige mit statischen Werten und einige mit dynamischen Werten, die ein Benutzer ändern kann. Die meisten Steuerelemente können Eigenschaften zugeordnet werden, die mit der **IMAPIProp** -Implementierung verwaltet werden. Wenn ein Benutzer den Wert eines änderbaren Steuerelements ändert, wird die entsprechende Eigenschaft aktualisiert. 
  
Dienstanbieter implementieren Anzeige Tabellen und die **IMAPIProp** -Schnittstelle. Das Erstellen einer Anzeigetabelle ähnelt dem Schreiben eines Programms mit einer Skriptsprache. Dienstanbieter können eine Anzeigetabelle erstellen, indem Sie: 
  
- Aufrufen der [BuildDisplayTable](builddisplaytable.md) -Funktion. 
    
    - Oder
    
- Einschließlich benutzerdefinierter Code, der die Anzeigetabelle direkt mit einem Tabellendaten Objekt auffüllt – ein Objekt, das die [ITableData: IUnknown](itabledataiunknown.md) -Schnittstelle unterstützt. 
    
Die **BuildDisplayTable** -Funktion kombiniert Informationen aus Anzeige Tabellenstrukturen mit visuellen Elementen aus einer Dialogfeldressource, um Tabellenzeilen anzuzeigen. Die Funktion gibt einen Zeiger auf eine [IMAPITable: IUnknown](imapitableiunknown.md) -Schnittstellenimplementierung und, falls erforderlich, einen Zeiger auf eine **ITableData** -Schnittstellenimplementierung zurück. 
  
Die Verwendung von **BuildDisplayTable** zum Erstellen einer Anzeigetabelle ist einfach und erleichtert die Wartung, wenn sich visuelle Elemente der Anzeige ändern. Dienstanbieter, die **BuildDisplayTable** nicht verwenden möchten, können jedoch eine Anzeigetabelle mit benutzerdefiniertem Code erstellen, der die Methoden von **ITableData**verwendet. Beispielsweise können Dienstanbieter, die über eine vorhandene Vorlagenstruktur für Ihre Eigenschaftenseiten verfügen, benutzerdefinierten Code erstellen, statt **BuildDisplayTable**zu verwenden.
  
Es gibt unterschiedliche Möglichkeiten, wie Dienstanbieter die Eigenschaften Schnittstelle für Ihre Anzeigetabelle implementieren können. Zu diesen zählen:
  
- Angeben einer standardmäßigen [IMAPIProp: IUnknown](imapipropiunknown.md) -Implementierung. 
    
- Bereitstelleneiner eingebundenen **IMAPIProp** -Implementierung, die eine spezielle Verarbeitung enthält, bevor Sie die Standard Aufrufe ausführen. 
    
- Bereitstelleneiner [IPropData: IMAPIProp](ipropdataimapiprop.md) -Implementierung. 
    
Die Art der Implementierung hängt von den Eigenschaften der anzuzeigenden Daten und dem Verantwortlichen Dienstanbieter ab. Wenn beispielsweise eine implizite Beziehung zwischen den Daten in zwei Bearbeitungssteuerelementen vorhanden ist und eines der Steuerelemente geändert wird, muss die **IMAPIProp** -Implementierung den Wert des anderen Steuerelements entsprechend ändern. 
  
Anzeige Tabellen weisen die folgenden Eigenschaften im erforderlichen Spaltensatz auf:
  
|||
|:-----|:-----|
|**PR_XPOS** ([Pidtagxcoordinate (](pidtagxcoordinate-canonical-property.md))  <br/> |**PR_YPOS** ([Pidtagycoordinate (](pidtagycoordinate-canonical-property.md))  <br/> |
|**PR_DELTAX** ([Pidtagdeltax (](pidtagdeltax-canonical-property.md))  <br/> |**PR_DELTAY** ([Pidtagdeltay (](pidtagdeltay-canonical-property.md))  <br/> |
|**PR_CONTROL_TYPE** ([Pidtagcontroltype (](pidtagcontroltype-canonical-property.md))  <br/> |**PR_CONTROL_FLAGS** ([Pidtagcontrolflags (](pidtagcontrolflags-canonical-property.md))  <br/> |
|**PR_CONTROL_STRUCTURE** ([Pidtagcontrolstructure (](pidtagcontrolstructure-canonical-property.md))  <br/> |**PR_CONTROL_ID** ([Pidtagcontrolid (](pidtagcontrolid-canonical-property.md))  <br/> |
   
 **PR_XPOS** und **PR_YPOS** geben die X-und Y-Koordinaten der oberen linken Ecke des Steuerelements an. Die horizontalen Einheiten sind 1/4 der Dialogfeld-Basis-breiten Einheit; die vertikalen Einheiten sind 1/8 der Dialogbasis-Höheneinheit. Windows berechnet die aktuellen Dialogbasis Einheiten von der Höhe und Breite der aktuellen Systemschriftart. Die Koordinaten sind relativ zum Ursprung des Eigenschaftenseiten Bereichs. Die Größe der Eigenschaftenseiten ist auf ungefähr 200 von 180 Dialogeinheiten begrenzt. 
  
 **PR_DELTAX** und **PR_DELTAY** sind die Breite und Höhe des Steuerelements. Dies sind ULONG-Werte. Die breiten Einheiten sind 1/4 der Dialogfeld-Basis-breiten Einheit; die Höheneinheiten sind 1/8 der Dialogbasis-Höheneinheit. Die Koordinaten sind relativ zum Ursprung des Steuerelements. 
  
Die anderen vier Eigenschaften beschreiben verschiedene Merkmale des Steuerelements. **PR_CONTROL_TYPE** gibt den Typ des Steuerelements an. MAPI definiert zwölf Typen von Steuerelementen mit jeweils unterschiedlichen Attributen. Diese Attribute werden in der Flags-Eigenschaft **PR_CONTROL_FLAGS**beschrieben. Beispiele für Attribute sind, ob ein Steuerelement bearbeitet oder erforderlich ist. 
  
Die Steuerelementstruktur, **PR_CONTROL_STRUCTURE**, enthält Informationen, die für den jeweiligen Steuerelementtyp relevant sind. Jeder Steuerelementtyp wird in einer anderen Struktur beschrieben. Beispielsweise werden Bearbeitungssteuerelemente mit der [DTBLEDIT](dtbledit.md) -Struktur beschrieben. **DTBLEDIT** -Strukturen enthalten Member, die die Anzahl von und bestimmten Typen von Zeichen, die auf das Steuerelement und ein Property-Tag, das die Eigenschaft identifiziert, deren Wert im Steuerelement angezeigt werden kann. **PR_CONTROL_STRUCTURE** wird als binäre Eigenschaft gespeichert. 
  
Der Steuerelementbezeichner, **PR_CONTROL_ID**, identifiziert das Steuerelement in dem von der Anzeigetabelle beschriebenen Dialogfeld eindeutig. **PR_CONTROL_ID** wird aus den Werten im *LpbNotif* -und *cbNotif* -Member der [DTCTL](dtctl.md) -Struktur festgelegt, die von **BuildDisplayTable** zum Erstellen der Anzeigetabelle verwendet wird. Da MAPI manchmal Anzeige Tabellen kombiniert, sollte der Bezeichner in **PR_CONTROL_ID** immer eindeutig sein. In der Regel weisen Anbieter **PR_CONTROL_ID** eine [GUID](guid.md) -Struktur zu, um deren Eindeutigkeit sicherzustellen. Die **PR_CONTROL_ID** -Eigenschaft ist in der [TABLE_NOTIFICATION](table_notification.md) -Struktur enthalten, wenn eine Anzeige Tabellenbenachrichtigung generiert wird. 
  
Weitere Informationen zu Anzeige Tabellen finden Sie unter [Anzeige Tabellen Implementierung](display-table-implementation.md) und [Informationen zu Anzeige Tabellen Benachrichtigungen](about-display-table-notifications.md). 
  
## <a name="see-also"></a>Siehe auch



[MAPI-Tabellen](mapi-tables.md)

