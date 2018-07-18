---
title: Anzeigetabellen
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
localization_priority: Normal
api_type:
- COM
ms.assetid: c314ff6d-3e60-4b81-87ac-6ca6753ff633
description: 'Letzte �nderung: Montag, 9. M�rz 2015'
ms.openlocfilehash: 556d7551f64e075d1f15a945ddb1409c3b5a775f
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 06/11/2018
ms.locfileid: "19791589"
---
# <a name="display-tables"></a>Anzeigetabellen

  
  
**Betrifft**: Outlook 
  
Zeigt die Tabelle wird beschrieben, wie zum Anzeigen eines bestimmten Typs des Dialogfelds – eine müssen mindestens mit Registerkarten Eigenschaftenseiten zum Anzeigen und Bearbeiten von möglicherweise eine oder mehrere Eigenschaften. Verknüpft ist mit jedem Display-Tabelle ist eine [IMAPIProp: IUnknown](imapipropiunknown.md) Schnittstelle Implementierung. Die Implementierung **IMAPIProp** verwaltet die Daten, die angezeigt werden im Dialogfeld. 
  
Die Zeilen in einer Tabelle anzeigen darstellen, die Steuerelemente oder Schnittstelle Benutzerobjekte, die im Dialogfeld angezeigt werden. MAPI definiert viele andere Arten von Steuerelementen, einige mit statische Werte und einige mit dynamische Werte, die ein Benutzer ändern können. Die meisten Steuerelemente können mit der Implementierung **IMAPIProp** verwaltet Eigenschaften zugeordnet werden. Wenn ein Benutzer den Wert eines Steuerelements änderbare ändert, wird die entsprechende Eigenschaft aktualisiert. 
  
Dienstanbieter implementieren Anzeige Tabellen und die **IMAPIProp** -Schnittstelle. Erstellen einer Tabelle anzeigen ähnelt dem Schreiben eines Programms mit einer Skriptsprache. Dienstanbieter können eine Tabelle anzeigen, indem erstellen: 
  
- Aufrufen der [BuildDisplayTable](builddisplaytable.md) -Funktion. 
    
    - Oder -
    
- Benutzerdefinierten Code, der die direkt mit einem Datenobjekt Tabelle zeigt die Tabelle füllt einschließlich – ein Objekt, unterstützt die [ITableData: IUnknown](itabledataiunknown.md) Schnittstelle. 
    
Die Funktion **BuildDisplayTable** fasst Informationen aus Tabellenstrukturen anzeigen mit visuellen Elemente aus einer Ressource im Feld Display Tabellenzeilen erstellen. Die Funktion gibt einen Zeiger auf eine [IMAPITable: IUnknown](imapitableiunknown.md) Schnittstelle-Implementierung und, falls angefordert, einen Zeiger auf eine Implementierung **ITableData** . 
  
Verwenden zum Erstellen einer Tabelle anzeigen **BuildDisplayTable** ist einfach und Wartung vereinfacht, wenn visuelle Elemente der Anzeige ändern. Dienstanbieter, die nicht mit **BuildDisplayTable möchten** können jedoch eine zeigt die Tabelle mit benutzerdefiniertem Code erstellen, die die Methoden des **ITableData**verwendet. Beispielsweise könnten Dienstanbieter, die eine vorhandene Vorlagenstruktur für ihre Eigenschaftenseiten haben benutzerdefinierten Code erstellen, anstatt **BuildDisplayTable**zu verwenden.
  
Es gibt verschiedene Arten Dienstanbieter für ihre zeigt die Tabelle die Eigenschaft-Schnittstelle implementieren können. Dazu zählen folgende:
  
- Bereitstellen eines Standards [IMAPIProp: IUnknown](imapipropiunknown.md) Implementierung. 
    
- Bereitstellen einer gepackten **IMAPIProp** -Implementierung, die spezielle Verarbeitung vor der Durchführung der standard-Aufrufe enthält. 
    
- Bereitstellen einer [IPropData: IMAPIProp](ipropdataimapiprop.md) Implementierung. 
    
Die Art der Implementierung hängt davon ab, die Merkmale der Daten angezeigt werden und der Dienstanbieter verantwortlich. Beispielsweise muss Wenn eine implizite Beziehung zwischen den Daten in zwei Bearbeitungssteuerelemente besteht und eines der Steuerelemente ändert, die **IMAPIProp** Implementierung den Wert des anderen Steuerelements entsprechend ändern. 
  
Anzeige Tabellen weisen die folgenden Eigenschaften in ihren erforderliche Spalte festlegen:
  
|||
|:-----|:-----|
|**PR_XPOS** ([PidTagXCoordinate](pidtagxcoordinate-canonical-property.md))  <br/> |**PR_YPOS** ([PidTagYCoordinate](pidtagycoordinate-canonical-property.md))  <br/> |
|**PR_DELTAX** ([PidTagDeltaX](pidtagdeltax-canonical-property.md))  <br/> |**PR_DELTAY** ([PidTagDeltaY](pidtagdeltay-canonical-property.md))  <br/> |
|**PR_CONTROL_TYPE** ([PidTagControlType](pidtagcontroltype-canonical-property.md))  <br/> |**PR_CONTROL_FLAGS** ([PidTagControlFlags](pidtagcontrolflags-canonical-property.md))  <br/> |
|**PR_CONTROL_STRUCTURE** ([PidTagControlStructure](pidtagcontrolstructure-canonical-property.md))  <br/> |**PR_CONTROL_ID** ([PidTagControlId](pidtagcontrolid-canonical-property.md))  <br/> |
   
 **PR_XPOS** und **PR_YPOS** geben die X- und Y-Koordinaten der oberen linken Ecke des Steuerelements. Die horizontalen Einheiten sind 1/4 der Dialogfeld Basis Breite Einheit. die vertikalen Einheiten sind 1/8 der Dialogfeld Basis Höhe Einheit. Windows berechnet die aktuellen Dialogfeld Basiseinheiten aus die Höhe und Breite der aktuellen Systemschriftart. Die Koordinaten sind relativ zum Ursprung des Seitenbereichs Eigenschaft. Die Größe der Eigenschaftenseiten beträgt ungefähr 200 von 180 Dialogfeld Einheiten. 
  
 **PR_DELTAX** und **PR_DELTAY** sind die Breite und Höhe des Steuerelements. Dabei handelt es sich um ULONG Werte. Die Einheiten sind 1/4 der Dialogfeld Basis Breite Einheit. die Höheneinheiten sind 1/8 der Dialogfeld Basis Höhe Einheit. Die Koordinaten sind relativ zum Ursprung des Steuerelements. 
  
Die anderen vier Eigenschaften werden verschiedene Eigenschaften des Steuerelements beschrieben. **PR_CONTROL_TYPE** gibt den Typ des Steuerelements an. MAPI definiert zwölf Typen von Steuerelementen, jeweils mit einem anderen Satz von Attributen. Diese Attribute werden in der Flags-Eigenschaft **PR_CONTROL_FLAGS**beschrieben. Beispiele für Attribute sind, ob ein Steuerelement bearbeitet werden oder erforderlich ist oder nicht. 
  
Die Kontrollstruktur **PR_CONTROL_STRUCTURE**, enthält Informationen zu den bestimmten Typ des Steuerelements. Jede Art von Steuerelement wird mit einer anderen Struktur beschrieben. Beispielsweise werden Edit-Steuerelemente mit der Struktur [DTBLEDIT](dtbledit.md) beschrieben. **DTBLEDIT** Strukturen enthalten Mitglieder dieser Liste der Anzahl und bestimmte Typen von Zeichen, die platziert werden können, klicken Sie auf das Steuerelement und ein Eigenschaftentag, das die Eigenschaft identifiziert, dessen Wert ist, die im Steuerelement angezeigt werden. **PR_CONTROL_STRUCTURE** wird als eine binäre Eigenschaft gespeichert. 
  
Die Steuerelement-ID, **PR_CONTROL_ID**, wird das Steuerelement beschrieben, die von der Tabelle anzeigen im Dialogfeld eindeutig identifiziert. **PR_CONTROL_ID** ist im *LpbNotif* und *CbNotif* -Member der [DTCTL](dtctl.md) -Struktur, die von **BuildDisplayTable** , zum Erstellen einer Tabelle anzeigen verwendet wird platzierten Werte festgelegt. Da MAPI manchmal Anzeige Tabellen kombiniert, sollte der Bezeichner in **PR_CONTROL_ID** immer eindeutig sein. Anbieter weisen in der Regel eine [GUID](guid.md) -Struktur **PR_CONTROL_ID** , um die Eindeutigkeit sicherzustellen. Die **PR_CONTROL_ID** -Eigenschaft ist in der Struktur [TABLE_NOTIFICATION](table_notification.md) enthalten, wenn eine Anzeige Tabelle Benachrichtigung generiert wird. 
  
Weitere Informationen zu Tabellen anzeigen finden Sie unter [Anzeigen von Tabelle Implementierung](display-table-implementation.md) und [Zum Anzeigen von Tabelle Benachrichtigungen](about-display-table-notifications.md). 
  
## <a name="see-also"></a>Siehe auch



[MAPI-Tabellen](mapi-tables.md)

