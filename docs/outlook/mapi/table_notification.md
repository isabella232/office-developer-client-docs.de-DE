---
title: TABLE_NOTIFICATION
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
ms.localizationpriority: medium
api_name:
- MAPI.TABLE_NOTIFICATION
api_type:
- COM
ms.assetid: 48e478c4-6e9a-40ab-a7bb-e6219b743b08
description: 'Letzte Änderung: Montag, 9. März 2015'
ms.openlocfilehash: b8141b1030d9e531aeb6e4be7e952edb4fa496e1
ms.sourcegitcommit: a1d9041c20256616c9c183f7d1049142a7ac6991
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 09/24/2021
ms.locfileid: "59566325"
---
# <a name="table_notification"></a>TABLE_NOTIFICATION

**Gilt für**: Outlook 2013 | Outlook 2016 
  
Beschreibt eine Zeile in einer Tabelle, die von einem Bestimmten Ereignistyp betroffen ist, z. B. eine Änderung oder ein Fehler. Dadurch wird eine Tabellenbenachrichtigung generiert. 
  
|||
|:-----|:-----|
|Headerdatei  <br/> |Mapidefs.h  <br/> |
   
```cpp
typedef struct _TABLE_NOTIFICATION
{
  ULONG ulTableEvent;
  HRESULT hResult;
  SPropValue propIndex;
  SPropValue propPrior;
  SRow row;
} TABLE_NOTIFICATION;

```

## <a name="members"></a>Members

**ulTableEvent**
  
> Bitmaske mit Flags, die zum Darstellen des Tabellenereignistyps verwendet werden. Die folgenden Flags können festgelegt werden:
    
TABLE_CHANGED 
  
> Gibt auf hoher Ebene an, dass sich etwas an der Tabelle geändert hat. Der Zustand der Tabelle ist wie vor dem Ereignis. Dies bedeutet, dass alle **PR_INSTANCE_KEY** ([PidTagInstanceKey](pidtaginstancekey-canonical-property.md)) -Eigenschaften, Lesezeichen, aktuelle Positionierung und Auswahl der Benutzeroberfläche weiterhin gültig sind. Behandeln Sie dieses Ereignis, indem Sie die Tabelle erneut lesen. Dienstanbieter, die keine Rich-Table-Benachrichtigungen implementieren möchten, senden TABLE_CHANGED Ereignisse anstelle detaillierterer Ereignisse, um auf eine bestimmte Art von Änderung hinzuweisen. 
    
TABLE_ERROR 
  
> Es ist ein Fehler aufgetreten, in der Regel während der Verarbeitung eines asynchronen Vorgangs. Fehler bei der Verarbeitung der folgenden Methoden können dieses Ereignis generieren: 
    
   - [IMAPITable::SortTable](imapitable-sorttable.md)
    
   - [IMAPITable::SetColumns](imapitable-setcolumns.md)
    
   - [IMAPITable::Restrict](imapitable-restrict.md)
    
   Nachdem ein TABLE_ERROR Ereignis empfangen wurde, kann sich ein Client nicht mehr auf die Genauigkeit des Tabelleninhalts verlassen. Außerdem gehen ausstehende Benachrichtigungen zu anderen Änderungen möglicherweise verloren. Die [IMAPITable::GetLastError-Methode](imapitable-getlasterror.md) stellt möglicherweise keine zusätzlichen Informationen zu dem Fehler bereit, da sie zu einem früheren Zeitpunkt generiert wurde, nicht unbedingt aus dem letzten Methodenaufruf. 
    
TABLE_RELOAD 
  
> Die Daten in der Tabelle sollten neu geladen werden. Dienstanbieter senden TABLE_RELOAD, wenn z. B. die zugrunde liegenden Daten in einer Datenbank gespeichert und die Datenbank ersetzt wird. Behandeln Sie dieses Ereignis, indem Sie davon ausgehen, dass nichts an der Tabelle noch gültig ist, und indem Sie die Tabelle erneut lesen. Alle Lesezeichen, Instanztasten, Status- und Positionierungsinformationen sind ungültig.
    
TABLE_RESTRICT_DONE 
  
> Ein mit einem **IMAPITable::Restrict-Methodenaufruf** initiierter Einschränkungsvorgang wurde abgeschlossen. 
    
TABLE_ROW_ADDED 
  
> Der Tabelle wurde eine neue Zeile hinzugefügt, und das entsprechende Objekt wurde gespeichert. TABLE_ROW_ADDED Ereignisse werden nach einem Aufruf der [IMAPIProp::SaveChanges-Methode](imapiprop-savechanges.md) generiert. 
    
TABLE_ROW_DELETED 
  
> Eine Zeile wurde aus der Tabelle entfernt. Das **propPrior-Element** ist auf NULL festgelegt. 
    
TABLE_ROW_MODIFIED 
  
> Eine Zeile wurde geändert. Das **Zeilenelement** enthält die betroffenen Eigenschaften für die Zeile. Mehrere TABLE_ROW_MODIFIED Ereignisse werden in der Reihenfolge gesendet, in der sie in der Tabellenansicht angezeigt werden. 
    
  TABLE_ROW_MODIFIED Ereignisse werden gesendet, nachdem Änderungen am entsprechenden Objekt mit einem Aufruf der **IMAPIProp::SaveChanges-Methode** ausgeführt wurden. Wenn die geänderte Zeile jetzt die erste Zeile in der Tabelle ist, ist der Wert des Eigenschaftstags im **propPrior-Element** **PR_NULL** ([PidTagNull](pidtagnull-canonical-property.md)).
    
TABLE_SETCOL_DONE 
  
> Ein mit einem **IMAPITable::SetColumns-Methodenaufruf initiierter Spalteneinstellungsvorgang** wurde abgeschlossen. 
    
TABLE_SORT_DONE 
  
> Ein mit einem **IMAPITable::SortTable-Methodenaufruf** initiierter Tabellensortierungsvorgang wurde abgeschlossen. 
    
**Hresult**
  
> HRESULT-Wert für den aufgetretenen Fehler, wenn der **ulTableEvent-Member** auf TABLE_ERROR festgelegt ist. 
    
**propIndex**
  
> [SPropValue-Struktur](spropvalue.md) für die **PR_INSTANCE_KEY** Eigenschaft der betroffenen Zeile. 
    
**propPrior**
  
> **SPropValue-Struktur** für die **PR_INSTANCE_KEY** Eigenschaft der Zeile vor der betroffenen Zeile. Wenn die betroffene Zeile die erste Zeile in der Tabelle ist, muss **propPrior** auf **PR_NULL** und nicht auf Null festgelegt werden. Null ist kein gültiges Eigenschaftstag. 
    
**Zeile**
  
> [SRow-Struktur,](srow.md) die die betroffene Zeile beschreibt. Diese Struktur ist für alle Tabellenbenachrichtigungsereignisse gefüllt. Bei Tabellenbenachrichtigungsereignissen, die keine Zeilendaten übergeben, wird das **cValues-Element** der **SRow-Struktur** auf Null und das **lpProps-Element** auf NULL festgelegt. Da diese **SRow-Struktur** schreibgeschützt ist; Clients müssen eine Kopie davon erstellen, wenn sie Änderungen vornehmen möchten. Die [ScDupPropset-Funktion](scduppropset.md) kann zum Erstellen der Kopie verwendet werden. 
    
## <a name="remarks"></a>HinwBemerkungeneise

Die **TABLE \_ NOTIFICATION-Struktur** ist eines der Mitglieder der Vereinigung von Strukturen, die im **Infoelement** der [NOTIFICATION-Struktur](notification.md) enthalten sind. Das **Info-Element** enthält eine **TABLE \_ NOTIFICATION-Struktur,** wenn das **ulEventType-Element** der Struktur auf  _fnevTableModified_ festgelegt ist.
  
Die Reihenfolge und der Spaltentyp im Zeilenelement geben die Reihenfolge und den Typ wieder, die zum Zeitpunkt der Benachrichtigungsgenerierung wirksam waren. Die Reihenfolge und der Typ zum Zeitpunkt der Benachrichtigungsgenerierung sind nicht unbedingt identisch mit dem Zeitpunkt, an dem die Benachrichtigung übermittelt wurde. 
  
Weitere Informationen zur Benachrichtigung finden Sie in den in der folgenden Tabelle beschriebenen Themen.
  
|**Thema**|**Beschreibung**|
|:-----|:-----|
|[Ereignisbenachrichtigung in MAPI](event-notification-in-mapi.md) <br/> |Allgemeine Übersicht über Benachrichtigungs- und Benachrichtigungsereignisse.  <br/> |
|[Behandeln von Benachrichtigungen](handling-notifications.md) <br/> |Erläuterung, wie Clients Benachrichtigungen behandeln sollten.  <br/> |
|[Unterstützende Ereignisbenachrichtigung](supporting-event-notification.md) <br/> |Erläuterung, wie Dienstanbieter die **IMAPISupport-Methode** zum Generieren von Benachrichtigungen verwenden können.  <br/> |
   
Da Tabellenbenachrichtigungen asynchron sind, können Clients eine Benachrichtigung über eine hinzugefügte Zeile erhalten, nachdem sie die Hinzufügung auf andere Weise gelernt haben. Es ist möglich, ein TABLE_ERROR Ereignis zu empfangen, wenn ein Fehler in einer **IMAPITable::Sort**, **IMAPITable::Restrict**- oder **IMAPITable::SetColumns-Methode** vorliegt oder wenn ein zugrunde liegender Prozess versucht, eine Tabelle zu aktualisieren, z. B. mit neuen oder geänderten Zeilen. 
  
## <a name="see-also"></a>Siehe auch

- [Benachrichtigung](notification.md) 
- [ScDupPropset](scduppropset.md)
- [SRow](srow.md)
- [SPropValue](spropvalue.md)
- [MAPI-Strukturen](mapi-structures.md)

