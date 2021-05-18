---
title: Anzeigen von Tabellen
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
# <a name="display-tables"></a>Anzeigen von Tabellen

  
  
**Gilt für**: Outlook 2013 | Outlook 2016 
  
In einer Anzeigetabelle wird beschrieben, wie sie einen bestimmten Typ von Dialogfeld anzeigen – eine mit einer oder mehreren Eigenschaftenseiten mit Registerkarten, die zum Anzeigen und bearbeiten einer oder mehreren Eigenschaften verwendet werden. Jeder Anzeigetabelle ist eine [IMAPIProp : IUnknown-Schnittstellenimplementierung](imapipropiunknown.md) zugeordnet. Die **IMAPIProp-Implementierung** verwaltet die Eigenschaftendaten, die im Dialogfeld angezeigt werden. 
  
Die Zeilen in einer Anzeigetabelle stellen die Steuerelemente oder Benutzeroberflächenobjekte dar, die im Dialogfeld angezeigt werden. MAPI definiert viele Arten von Steuerelementen, einige mit statischen Werten und einige mit dynamischen Werten, die ein Benutzer ändern kann. Die meisten Steuerelemente können Eigenschaften zugeordnet werden, die mit der **IMAPIProp-Implementierung verwaltet** werden. Wenn ein Benutzer den Wert eines veränderbaren Steuerelements ändert, wird die entsprechende Eigenschaft aktualisiert. 
  
Dienstanbieter implementieren Anzeigetabellen und die **IMAPIProp-Schnittstelle.** Das Erstellen einer Anzeigetabelle ähnelt dem Schreiben eines Programms mit einer Skriptsprache. Dienstanbieter können eine Anzeigetabelle erstellen, indem Sie: 
  
- Aufrufen der [BuildDisplayTable-Funktion.](builddisplaytable.md) 
    
    - Oder -
    
- Einschließlich benutzerdefinierten Codes, der die Anzeigetabelle direkt mithilfe eines Tabellendatenobjekts auffüllt – ein Objekt, das die [ITableData : IUnknown-Schnittstelle](itabledataiunknown.md) unterstützt. 
    
Die **BuildDisplayTable-Funktion** kombiniert Informationen aus Anzeigetabellenstrukturen mit visuellen Elementen aus einer Dialogfeldressource, um Anzeigetabellenzeilen zu erstellen. Die Funktion gibt einen Zeiger auf eine [IMAPITable : IUnknown-Schnittstellenimplementierung](imapitableiunknown.md) und, falls angefordert, einen Zeiger auf eine **ITableData-Schnittstellenimplementierung** zurück. 
  
Die **Verwendung von BuildDisplayTable** zum Erstellen einer Anzeigetabelle ist unkompliziert und erleichtert die Wartung, wenn sich visuelle Elemente der Anzeige ändern. Dienstanbieter, die **BuildDisplayTable** nicht verwenden möchten, können jedoch eine Anzeigetabelle mit benutzerdefiniertem Code erstellen, der die Methoden von **ITableData verwendet.** Beispielsweise möchten Dienstanbieter, die über eine vorhandene Vorlagenstruktur für ihre Eigenschaftenseiten verfügen, möglicherweise benutzerdefinierten Code erstellen, anstatt **BuildDisplayTable zu verwenden.**
  
Es gibt eine Vielzahl von Möglichkeiten, wie Dienstanbieter die Eigenschaftsschnittstelle für ihre Anzeigetabelle implementieren können. Zu diesen zählen:
  
- Bereitstellung einer [standardmäßigen IMAPIProp : IUnknown-Implementierung.](imapipropiunknown.md) 
    
- Bereitstellung einer umschlossenen **IMAPIProp-Implementierung,** die eine spezielle Verarbeitung vor den Standardaufrufen enthält. 
    
- Bereitstellung einer [IPropData : IMAPIProp-Implementierung.](ipropdataimapiprop.md) 
    
Der Typ der Implementierung hängt von den Merkmalen der daten, die angezeigt werden sollen, und vom zuständigen Dienstanbieter ab. Wenn beispielsweise eine implizite Beziehung zwischen den Daten in zwei Bearbeitungssteuerelementen besteht und eines der Steuerelemente geändert wird, muss die **IMAPIProp-Implementierung** den Wert des anderen Steuerelements entsprechend ändern. 
  
Anzeigetabellen haben die folgenden Eigenschaften in ihrem erforderlichen Spaltensatz:
  
|||
|:-----|:-----|
|**PR_XPOS** ([PidTagXCoordinate](pidtagxcoordinate-canonical-property.md))  <br/> |**PR_YPOS** ([PidTagYCoordinate](pidtagycoordinate-canonical-property.md))  <br/> |
|**PR_DELTAX** ([PidTagDeltaX](pidtagdeltax-canonical-property.md))  <br/> |**PR_DELTAY** ([PidTagDeltaY](pidtagdeltay-canonical-property.md))  <br/> |
|**PR_CONTROL_TYPE** ([PidTagControlType](pidtagcontroltype-canonical-property.md))  <br/> |**PR_CONTROL_FLAGS** ([PidTagControlFlags](pidtagcontrolflags-canonical-property.md))  <br/> |
|**PR_CONTROL_STRUCTURE** ([PidTagControlStructure](pidtagcontrolstructure-canonical-property.md))  <br/> |**PR_CONTROL_ID** ([PidTagControlId](pidtagcontrolid-canonical-property.md))  <br/> |
   
 **PR_XPOS** und **PR_YPOS** geben die X- und Y-Koordinaten der linken oberen Ecke des Steuerelements an. Die horizontalen Einheiten sind 1/4 der Dialogbasisbreiteneinheit. die vertikalen Einheiten sind 1/8 der Dialogbasishöheneinheit. Windows berechnet die aktuellen Dialogbasiseinheiten aus der Höhe und Breite der aktuellen Systemschriftart. Die Koordinaten sind relativ zum Ursprung des Eigenschaftenseitenbereichs. Die Größe von Eigenschaftenseiten ist auf ca. 200 bis 180 Dialogeinheiten beschränkt. 
  
 **PR_DELTAX** und **PR_DELTAY** sind die Breite und Höhe des Steuerelements. Dies sind ULONG-Werte. Die Breiteneinheiten sind 1/4 der Dialogbasisbreiteneinheit. die Höheneinheiten sind 1/8 der Dialogbasishöheneinheit. Die Koordinaten sind relativ zum Ursprung des Steuerelements. 
  
Die anderen vier Eigenschaften beschreiben verschiedene Merkmale des Steuerelements. **PR_CONTROL_TYPE** gibt den Typ des Steuerelements an. MAPI definiert zwölf Arten von Steuerelementen mit jeweils unterschiedlichen Attributen. Diese Attribute werden in der Flags-Eigenschaft beschrieben, **PR_CONTROL_FLAGS**. Beispiele für Attribute sind, ob ein Steuerelement bearbeitbar oder erforderlich ist. 
  
Die Steuerelementstruktur, **PR_CONTROL_STRUCTURE**, enthält Informationen, die für den jeweiligen Steuerelementtyp relevant sind. Jeder Steuerelementtyp wird mit einer anderen Struktur beschrieben. Beispielsweise werden Bearbeitungssteuerelemente mit der [DTBLEDIT-Struktur](dtbledit.md) beschrieben. **DTBLEDIT-Strukturen** enthalten Elemente, die die Anzahl und bestimmte Typen von Zeichen auflisten, die für das Steuerelement platziert werden können, und ein Eigenschaftentag, das die Eigenschaft identifiziert, deren Wert im Steuerelement angezeigt werden soll. **PR_CONTROL_STRUCTURE** wird als binäre Eigenschaft gespeichert. 
  
Die Steuerelement-ID, **PR_CONTROL_ID**, identifiziert das Steuerelement eindeutig im Dialogfeld, das von der Anzeigetabelle beschrieben wird. **PR_CONTROL_ID** wird aus den Werten in den  *LpbNotif-*  und  *cbNotif-Mitgliedern*  der [DTCTL-Struktur](dtctl.md) festgelegt, die von **BuildDisplayTable** zum Erstellen der Anzeigetabelle verwendet wird. Da MAPI manchmal Anzeigetabellen kombiniert, sollte der Bezeichner in **PR_CONTROL_ID** immer eindeutig sein. In der Regel weisen Anbieter eine [GUID-Struktur](guid.md) **PR_CONTROL_ID,** um ihre Eindeutigkeit sicherzustellen. Die **PR_CONTROL_ID-Eigenschaft** ist in der TABLE_NOTIFICATION [enthalten,](table_notification.md) wenn eine Anzeigetabelle generiert wird. 
  
Weitere Informationen zu Anzeigetabellen finden Sie unter [Display Table Implementation](display-table-implementation.md) und About Display Table [Notifications](about-display-table-notifications.md). 
  
## <a name="see-also"></a>Siehe auch



[MAPI-Tabellen](mapi-tables.md)

