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
# <a name="table_notification"></a>TABLE_NOTIFICATION

**Gilt für**: Outlook 2013 | Outlook 2016 
  
Beschreibt eine Zeile in einer Tabelle, die von einem bestimmten Ereignistyp betroffen ist, z. B. eine Änderung oder einen Fehler. Dadurch wird eine Tabellenbenachrichtigung generiert. 
  
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

## <a name="members"></a>Elemente

**ulTableEvent**
  
> Bitmaske von Flags, die zum Darstellen des Tabellenereignistyps verwendet werden. Die folgenden Kennzeichen können festgelegt werden:
    
TABLE_CHANGED 
  
> Gibt auf einer hohen Ebene an, dass sich etwas an der Tabelle geändert hat. Der Zustand der Tabelle ist so wie vor dem Ereignis. Dies bedeutet, **dass PR_INSTANCE_KEY** ([PidTagInstanceKey](pidtaginstancekey-canonical-property.md)) -Eigenschaften, Lesezeichen, aktuelle Positionierung und Auswahl der Benutzeroberflächen weiterhin gültig sind. Behandeln Sie dieses Ereignis, indem Sie die Tabelle erneut lesen. Dienstanbieter, die keine Rich-Table-Benachrichtigungen implementieren möchten, senden TABLE_CHANGED anstatt ausführlichere Ereignisse, um einen bestimmten Änderungstyp anzugeben. 
    
TABLE_ERROR 
  
> Ein Fehler ist aufgetreten, in der Regel während der Verarbeitung eines asynchronen Vorgangs. Fehler bei der Verarbeitung der folgenden Methoden können dieses Ereignis generieren: 
    
   - [IMAPITable::SortTable](imapitable-sorttable.md)
    
   - [IMAPITable::SetColumns](imapitable-setcolumns.md)
    
   - [IMAPITable::Restrict](imapitable-restrict.md)
    
   Nachdem ein TABLE_ERROR empfangen wurde, kann sich ein Client nicht mehr auf die Genauigkeit des Tabelleninhalts verlassen. Außerdem gehen ausstehende Benachrichtigungen zu anderen Änderungen möglicherweise verloren. Die [IMAPITable::GetLastError-Methode](imapitable-getlasterror.md) stellt möglicherweise keine zusätzlichen Informationen zu dem Fehler zur Verfügung, da er an einem früheren Punkt generiert wurde, nicht unbedingt aus dem letzten Methodenaufruf. 
    
TABLE_RELOAD 
  
> Die Daten in der Tabelle sollten neu geladen werden. Dienstanbieter senden TABLE_RELOAD, wenn beispielsweise die zugrunde liegenden Daten in einer Datenbank gespeichert und die Datenbank ersetzt wird. Behandeln Sie dieses Ereignis, indem Sie davon ausgegangen werden, dass nichts über die Tabelle noch gültig ist, und indem Sie die Tabelle erneut lesen. Alle Lesezeichen, Instanzschlüssel, Status- und Positionierungsinformationen sind ungültig.
    
TABLE_RESTRICT_DONE 
  
> Ein Einschränkungsvorgang, der mit einem **IMAPITable::Restrict-Methodenaufruf** initiiert wurde, wurde abgeschlossen. 
    
TABLE_ROW_ADDED 
  
> Der Tabelle wurde eine neue Zeile hinzugefügt und das entsprechende Objekt gespeichert. TABLE_ROW_ADDED werden nach einem Aufruf der [IMAPIProp::SaveChanges-Methode](imapiprop-savechanges.md) generiert. 
    
TABLE_ROW_DELETED 
  
> Eine Zeile wurde aus der Tabelle entfernt. Das **propPrior-Element** ist auf NULL festgelegt. 
    
TABLE_ROW_MODIFIED 
  
> Eine Zeile wurde geändert. Das **Zeilenm** member enthält die betroffenen Eigenschaften für die Zeile. Mehrere TABLE_ROW_MODIFIED werden in der Reihenfolge gesendet, in der sie in der Tabellenansicht angezeigt werden. 
    
  TABLE_ROW_MODIFIED werden gesendet, nachdem Änderungen am entsprechenden Objekt mit einem Aufruf der **IMAPIProp::SaveChanges-Methode ausgeführt** wurden. Wenn die geänderte Zeile jetzt die erste Zeile in der Tabelle ist, ist der Wert des Eigenschaftstags im **propPrior-Element** **PR_NULL** ([PidTagNull](pidtagnull-canonical-property.md)).
    
TABLE_SETCOL_DONE 
  
> Ein Spalteneinstellungsvorgang, der mit einem **IMAPITable::SetColumns-Methodenaufruf** initiiert wurde, wurde abgeschlossen. 
    
TABLE_SORT_DONE 
  
> Ein mit einem **IMAPITable::SortTable-Methodenaufruf** initiierter Tabellensortierungsvorgang wurde abgeschlossen. 
    
**hResult**
  
> HRESULT-Wert für den aufgetretenen Fehler, wenn das **ulTableEvent-Element** auf TABLE_ERROR. 
    
**propIndex**
  
> [SPropValue-Struktur](spropvalue.md) für **die PR_INSTANCE_KEY-Eigenschaft** der betroffenen Zeile. 
    
**propPrior**
  
> **SPropValue-Struktur** für **die PR_INSTANCE_KEY-Eigenschaft** der Zeile vor der betroffenen. Wenn die betroffene Zeile die erste Zeile in der Tabelle ist, muss **propPrior** auf PR_NULL **und** nicht auf Null festgelegt werden. Null ist kein gültiges Eigenschaftstag. 
    
**row**
  
> [SRow-Struktur,](srow.md) die die betroffene Zeile beschreibt. Diese Struktur wird für alle Tabellenbenachrichtigungsereignisse gefüllt. Bei Tabellenbenachrichtigungsereignissen, die keine Zeilendaten übergeben, wird **das cValues-Element** der **SRow-Struktur** auf Null und das **lpProps-Element** auf NULL festgelegt. Da diese **#A0** schreibgeschützt ist; clients must make a copy of it if they want to make modifications. Die [ScDupPropset-Funktion](scduppropset.md) kann zum Erstellen der Kopie verwendet werden. 
    
## <a name="remarks"></a>Hinweise

Die **STRUKTUR TABLE \_ NOTIFICATION** ist eines der Mitglieder der Strukturgewerkschaft, die im **Infom** member der [NOTIFICATION-Struktur enthalten](notification.md) ist. Das **Element info** enthält eine TABLE **\_ NOTIFICATION-Struktur,** wenn **das ulEventType-Element** der Struktur auf _fnevTableModified festgelegt ist._
  
Die Reihenfolge und der Typ der Spalten im Zeilenm member spiegeln die Reihenfolge und den Typ wider, die zum Zeitpunkt der Benachrichtigung generiert wurden. Die Reihenfolge und der Typ zum Zeitpunkt der Benachrichtigung sind nicht unbedingt identisch mit dem Zeitpunkt, zu dem die Benachrichtigung zugestellt wurde. 
  
Weitere Informationen zur Benachrichtigung finden Sie in den In der folgenden Tabelle beschriebenen Themen.
  
|**Thema**|**Beschreibung**|
|:-----|:-----|
|[Ereignisbenachrichtigung in MAPI](event-notification-in-mapi.md) <br/> |Allgemeine Übersicht über Benachrichtigungs- und Benachrichtigungsereignisse.  <br/> |
|[Behandeln von Benachrichtigungen](handling-notifications.md) <br/> |Diskussion darüber, wie Clients mit Benachrichtigungen umgehen sollten.  <br/> |
|[Unterstützende Ereignisbenachrichtigung](supporting-event-notification.md) <br/> |Hier erfahren Sie, wie Dienstanbieter die **IMAPISupport-Methode** zum Generieren von Benachrichtigungen verwenden können.  <br/> |
   
Da Tabellenbenachrichtigungen asynchron sind, können Clients eine Benachrichtigung über eine hinzugefügte Zeile erhalten, nachdem sie über eine andere Möglichkeit von der Ergänzung gelernt haben. Es ist möglich, ein TABLE_ERROR-Ereignis zu empfangen, wenn ein Fehler in einer **IMAPITable::Sort-,** **IMAPITable::Restrict-** oder **IMAPITable::SetColumns-Methode** auftritt oder wenn ein zugrunde liegender Prozess versucht, eine Tabelle mit z. B. neuen oder geänderten Zeilen zu aktualisieren. 
  
## <a name="see-also"></a>Siehe auch

- [Benachrichtigung](notification.md) 
- [ScDupPropset](scduppropset.md)
- [SRow](srow.md)
- [SPropValue](spropvalue.md)
- [MAPI-Strukturen](mapi-structures.md)

