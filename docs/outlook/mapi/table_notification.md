---
title: TABLE_NOTIFICATION
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- MAPI.TABLE_NOTIFICATION
api_type:
- COM
ms.assetid: 48e478c4-6e9a-40ab-a7bb-e6219b743b08
description: 'Letzte Änderung: Montag, 9. März 2015'
ms.openlocfilehash: 6c35220529fb88b470c563a0b004bfcf7e63ef76
ms.sourcegitcommit: 8657170d071f9bcf680aba50b9c07f2a4fb82283
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 04/28/2019
ms.locfileid: "33415957"
---
# <a name="tablenotification"></a>TABLE_NOTIFICATION

**Gilt für**: Outlook 2013 | Outlook 2016 
  
Beschreibt eine Zeile in einer Tabelle, die von einer Art von Ereignis beeinflusst wurde, beispielsweise eine Änderung oder ein Fehler. Dadurch wird eine Tabellenbenachrichtigung generiert. 
  
|||
|:-----|:-----|
|Headerdatei  <br/> |Mapidefs. h  <br/> |
   
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
  
> Bitmaske der Flags, die zum Darstellen des Table-Ereignistyps verwendet werden. Die folgenden Flags können festgelegt werden:
    
TABLE_CHANGED 
  
> Gibt auf hoher Ebene an, dass sich etwas in der Tabelle geändert hat. Der Status der Tabelle ist wie vor dem Ereignis. Dies führt dazu, dass alle **PR_INSTANCE_KEY** ([pidtaginstancekey (](pidtaginstancekey-canonical-property.md))-Eigenschaften, Lesezeichen, aktuelle Positionierung und Benutzeroberflächenauswahl noch gültig sind. Behandeln Sie dieses Ereignis, indem Sie die Tabelle erneut lesen. Dienstanbieter, die Rich-Table-Benachrichtigungen nicht implementieren möchten, senden TABLE_CHANGED-Ereignisse anstelle detaillierter Ereignisse, um einen bestimmten Änderungstyp anzugeben. 
    
TABLE_ERROR 
  
> Es ist ein Fehler aufgetreten, normalerweise während der Verarbeitung eines asynchronen Vorgangs. Fehler bei der Verarbeitung der folgenden Methoden können dieses Ereignis generieren: 
    
   - [IMAPITable::SortTable](imapitable-sorttable.md)
    
   - [IMAPITable::SetColumns](imapitable-setcolumns.md)
    
   - [IMAPITable::Restrict](imapitable-restrict.md)
    
   Nachdem ein TABLE_ERROR-Ereignis empfangen wurde, kann sich ein Client nicht auf die Genauigkeit des Tabelleninhalts verlassen. Außerdem können ausstehende Benachrichtigungen über andere Änderungen verloren gehen. Die [IMAPITable:: getlasterroraufzurufen](imapitable-getlasterror.md) -Methode bietet möglicherweise keine zusätzlichen Informationen zu dem Fehler, da Sie zu einem früheren Zeitpunkt generiert wurde, nicht unbedingt vom letzten Methodenaufruf. 
    
TABLE_RELOAD 
  
> Die Daten in der Tabelle sollten erneut geladen werden. Dienstanbieter senden TABLE_RELOAD, wenn beispielsweise die zugrunde liegenden Daten in einer Datenbank gespeichert sind und die Datenbank ersetzt wird. Behandeln Sie dieses Ereignis, indem Sie davon ausgehen, dass nichts zur Tabelle noch gültig ist und die Tabelle erneut gelesen wird. Alle Lesezeichen, Instanzenschlüssel, Status-und Positionierungsinformationen sind ungültig.
    
TABLE_RESTRICT_DONE 
  
> Ein mit einem **IMAPITable:: Restrict** -Methodenaufruf initiierter Einschränkungs Vorgang wurde abgeschlossen. 
    
TABLE_ROW_ADDED 
  
> Der Tabelle wurde eine neue Zeile hinzugefügt, und das entsprechende Objekt wurde gespeichert. TABLE_ROW_ADDED-Ereignisse werden nach einem Aufruf der [IMAPIProp:: SaveChanges](imapiprop-savechanges.md) -Methode generiert. 
    
TABLE_ROW_DELETED 
  
> Eine Zeile wurde aus der Tabelle entfernt. Das **propPrior** -Element ist auf NULL festgelegt. 
    
TABLE_ROW_MODIFIED 
  
> Eine Zeile wurde geändert. Das **Row** -Element enthält die betroffenen Eigenschaften für die Zeile. Mehrere TABLE_ROW_MODIFIED-Ereignisse werden in der Reihenfolge gesendet, in der Sie in der Tabellenansicht angezeigt werden. 
    
  TABLE_ROW_MODIFIED-Ereignisse werden gesendet, nachdem Änderungen am entsprechenden Objekt mit einem Aufruf der **IMAPIProp:: SaveChanges** -Methode übergeben wurden. Wenn die geänderte Zeile jetzt die erste Zeile in der Tabelle ist, ist der Wert des Property-Tags im **propPrior** -Element **PR_NULL** ([pidtagnull (](pidtagnull-canonical-property.md)).
    
TABLE_SETCOL_DONE 
  
> Ein mit einem **IMAPITable::** SetColumns-Methodenaufruf initiierter Spalten Einstellungsvorgang wurde abgeschlossen. 
    
TABLE_SORT_DONE 
  
> Ein Tabellen Sortiervorgang, der mit einem **IMAPITable:: sortable** -Methodenaufruf initiiert wurde, wurde abgeschlossen. 
    
**hResult**
  
> HRESULT-Wert für den aufgetretenen Fehler, wenn das **ulTableEvent** -Element auf TABLE_ERROR festgelegt ist. 
    
**propIndex**
  
> [SPropValue](spropvalue.md) -Struktur für die **PR_INSTANCE_KEY** -Eigenschaft der betroffenen Zeile. 
    
**propPrior**
  
> **SPropValue** -Struktur für die **PR_INSTANCE_KEY** -Eigenschaft der Zeile vor dem betroffenen. Wenn die betroffene Zeile die erste Zeile in der Tabelle ist, muss **propPrior** auf **PR_NULL** und nicht auf NULL festgelegt sein. NULL ist kein gültiges Property-Tag. 
    
**Zeile**
  
> [SRow](srow.md) -Struktur, die die betroffene Zeile beschreibt. Diese Struktur wird für alle Benachrichtigungsereignisse für Tabellen ausgefüllt. Für Tabellen Benachrichtigungsereignisse, die keine Zeilendaten überschreiten, wird das **cValues** -Element der **SRow** -Struktur auf NULL festgelegt, und das **LPPROPS** -Element wird auf NULL festgelegt. Da diese **SRow** -Struktur schreibgeschützt ist; Clients müssen eine Kopie davon erstellen, wenn Sie Änderungen vornehmen möchten. Die [ScDupPropset](scduppropset.md) -Funktion kann verwendet werden, um die Kopie zu erstellen. 
    
## <a name="remarks"></a>Bemerkungen

Die **Tabellen\_Benachrichtigungs** Struktur ist ein Mitglied der Vereinigung der Strukturen, die im **Info** -Element der Benachrichtigungs [](notification.md) Struktur enthalten sind. Der **Info** -Member enthält **eine\_Tabellen Benachrichtigungs** Struktur, wenn das **ulEventType** -Element der Struktur auf _fnevTableModified_festgelegt ist.
  
Die Reihenfolge und der Typ der Spalten im row-Element geben die Reihenfolge und den Typ wieder, die zu dem Zeitpunkt wirksam waren, zu dem die Benachrichtigung generiert wurde. Die Reihenfolge und der Typ zu dem Zeitpunkt, zu dem die Benachrichtigung generiert wurde, entsprechen nicht unbedingt dem Zeitpunkt, zu dem die Benachrichtigung übermittelt wurde. 
  
Weitere Informationen zur Benachrichtigung finden Sie in den in der folgenden Tabelle beschriebenen Themen.
  
|**Thema**|**Beschreibung**|
|:-----|:-----|
|[Ereignisbenachrichtigung in MAPI](event-notification-in-mapi.md) <br/> |Allgemeine Übersicht über Benachrichtigungs-und Benachrichtigungsereignisse.  <br/> |
|[Behandeln von Benachrichtigungen](handling-notifications.md) <br/> |Erläuterung, wie Clients Benachrichtigungen behandeln sollen.  <br/> |
|[Unterstützende Ereignisbenachrichtigung](supporting-event-notification.md) <br/> |Erläuterung, wie Dienstanbieter die **IMAPISupport** -Methode verwenden können, um Benachrichtigungen zu generieren.  <br/> |
   
Da Tabellen Benachrichtigungen asynchron sind, können Clients Benachrichtigungen über eine hinzugefügte Zeile erhalten, nachdem Sie über das Hinzufügen auf eine andere Weise informiert wurden. Es ist möglich, ein TABLE_ERROR-Ereignis zu empfangen, wenn ein Fehler in einer **IMAPITable:: Sort**, **IMAPITable:: Restrict**oder **IMAPITable::** SetColumns-Methode vorliegt oder wenn ein zugrunde liegender Prozess versucht, eine Tabelle mit zu aktualisieren, beispielsweise neue oder geänderte Zeilen. 
  
## <a name="see-also"></a>Siehe auch

- [Benachrichtigung](notification.md) 
- [ScDupPropset](scduppropset.md)
- [SRow](srow.md)
- [SPropValue](spropvalue.md)
- [MAPI-Strukturen](mapi-structures.md)

