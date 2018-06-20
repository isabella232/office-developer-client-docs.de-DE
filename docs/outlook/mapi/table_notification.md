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
description: 'Letzte �nderung: Montag, 9. M�rz 2015'
ms.openlocfilehash: fd77473ce728a51220a4c039f1d12d03d90e7f36
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 06/11/2018
ms.locfileid: "19795717"
---
# <a name="tablenotification"></a>TABLE_NOTIFICATION

**Betrifft**: Outlook 
  
Beschreibt eine Zeile in einer Tabelle, die mit einem Typ des Ereignisses, wie eine Änderung oder einen Fehler betroffen ist. Daraufhin wird eine Tabelle Benachrichtigung generiert werden soll. 
  
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
  
> Bitmaske aus Flags verwendet, um den Ereignistyp Tabelle darstellen. Die folgenden Kennzeichen können festgelegt werden:
    
TABLE_CHANGED 
  
> Gibt auf allgemeiner Ebene, dass etwas über die Tabelle geändert hat. Die Tabelle festgelegt ist, wie er vor dem das Ereignis. Dies bedeutet, dass alle Eigenschaften **PR_INSTANCE_KEY** ([PidTagInstanceKey](pidtaginstancekey-canonical-property.md)), Lesezeichen, aktuellen Positionierung und Schnittstelle Benutzerauswahl noch gültig sind. Behandeln Sie dieses Ereignis wird durch erneutes Lesen der Tabelle. Dienstanbieter, die keine rich Tabelle Benachrichtigungen implementieren möchten, senden TABLE_CHANGED Ereignisse anstelle von ausführlichere Ereignisse zum Angeben eines bestimmten Typs der Änderung. 
    
TABLE_ERROR 
  
> In der Regel während der Verarbeitung eines asynchronen Vorgangs ist ein Fehler aufgetreten. Fehler bei der Verarbeitung der folgenden Methoden können dieses Ereignis generieren: 
    
   - [SortTable](imapitable-sorttable.md)
    
   - [IMAPITable::SetColumns](imapitable-setcolumns.md)
    
   - [Methode IMAPITable:: Restrict](imapitable-restrict.md)
    
   Ein Client kann nicht nach dem Empfang ein TABLE_ERROR-Ereignis, auf die Genauigkeit der Inhalt der Tabelle verlassen. Darüber hinaus möglicherweise ausstehende Benachrichtigungen zu anderen Änderungen verloren. Die [IMAPITable::GetLastError](imapitable-getlasterror.md) -Methode bietet zusätzliche Informationen zu dem Fehler möglicherweise nicht, da es zu einem Zeitpunkt, was nicht notwendigerweise vom letzten Methodenaufruf generiert wurde. 
    
TABLE_RELOAD 
  
> Die Daten in der Tabelle sollte erneut geladen werden. Dienstanbieter senden TABLE_RELOAD, wenn beispielsweise die zugrunde liegenden Daten in einer Datenbank gespeichert ist und die Datenbank ersetzt wird. Behandeln Sie dieses Ereignis von, unter der Annahme, dass nichts über die Tabelle noch gültig ist und durch erneutes Lesen der Tabelle. Alle Lesezeichen, Instanzenschlüssel, Status und Positionierung Informationen sind ungültig.
    
TABLE_RESTRICT_DONE 
  
> Eine Einschränkung, die mit einem Aufruf der **Methode IMAPITable:: Restrict** -Methode initiiert wurde abgeschlossen. 
    
TABLE_ROW_ADDED 
  
> Eine neue Zeile wurde der Tabelle und das entsprechende Objekt gespeichert hinzugefügt. TABLE_ROW_ADDED Ereignisse werden nach einem Aufruf der [IMAPIProp::SaveChanges](imapiprop-savechanges.md) -Methode generiert. 
    
TABLE_ROW_DELETED 
  
> Eine Zeile wurde aus der Tabelle entfernt. Das **PropPrior** -Element wird auf NULL festgelegt. 
    
TABLE_ROW_MODIFIED 
  
> Eine Zeile wurde geändert. **Das Zeilenelement** enthält die betroffenen Eigenschaften für die Zeile. Mehrere TABLE_ROW_MODIFIED-Ereignisse werden in der Reihenfolge gesendet, die sie in der Tabellenansicht angezeigt werden. 
    
  TABLE_ROW_MODIFIED Ereignisse werden gesendet, nachdem Änderungen an das entsprechende Objekt mit einem Aufruf der **IMAPIProp::SaveChanges** -Methode übergeben wurden. Wenn die geänderte Zeile jetzt die erste Zeile in der Tabelle ist, ist der Wert des Tags-Eigenschaft im **PropPrior** -Member **PR_NULL** ([PidTagNull](pidtagnull-canonical-property.md)).
    
TABLE_SETCOL_DONE 
  
> Eine Spalte Einstellung, die mit einem Aufruf der **IMAPITable::SetColumns** -Methode initiiert wurde abgeschlossen. 
    
TABLE_SORT_DONE 
  
> Eine Tabelle sortieren Vorgang mit einem Aufruf der **SortTable** -Methode initiiert wurde abgeschlossen. 
    
**hResult**
  
> HRESULT-Wert für den, der aufgetretenen Fehler, wenn das Element **UlTableEvent** auf TABLE_ERROR festgelegt ist. 
    
**propIndex**
  
> [SPropValue](spropvalue.md) -Struktur für die **PR_INSTANCE_KEY** -Eigenschaft der betreffenden Zeile. 
    
**propPrior**
  
> **SPropValue** -Struktur für die **PR_INSTANCE_KEY** -Eigenschaft der Zeile vor der betroffenen. Wenn die betroffene Zeile der ersten Zeile in der Tabelle ist, muss **PropPrior** **PR_NULL** und nicht 0 (null) festgelegt werden. 0 (null) ist eine gültige Eigenschaftentag. 
    
**Zeile**
  
> [SRow](srow.md) -Struktur, die die betreffenden Zeile beschreibt. Diese Struktur ist für alle Tabelle Benachrichtigungsereignisse gefüllt. Für Benachrichtigungsereignisse der Tabelle, die keine Zeilendaten übergeben, das **cValues** Mitglied der **SRow** -Struktur auf 0 (null) festgelegt ist und der **LpProps** Member wird auf NULL festgelegt. Da diese Struktur **SRow** schreibgeschützt ist. Clients müssen eine Kopie davon vornehmen, wenn sie Änderungen vornehmen möchten. Die [ScDupPropset](scduppropset.md) -Funktion kann verwendet werden, um die Kopie zu erstellen. 
    
## <a name="remarks"></a>Hinweise

Die **Tabelle\_Benachrichtigung** Struktur ist ein Mitglied der Union der Strukturen, die in der **Info** -Member der Struktur [Benachrichtigung](notification.md) enthalten. Das **Info** -Element enthält eine **Tabelle\_Benachrichtigung** Struktur, wenn der **UlEventType** Member der Struktur auf _FnevTableModified_festgelegt ist.
  
Die Reihenfolge und den Typ der Spalten in der Zeile Member entsprechen die Reihenfolge und den Typ, der zum Zeitpunkt gültig war, die die Benachrichtigung generiert wurde. Die Reihenfolge und den Typ der Zeitpunkt, die die Benachrichtigung generiert wurde ist nicht unbedingt identisch, wenn die Benachrichtigung übermittelt wurde. 
  
Weitere Informationen zur Benachrichtigung finden Sie unter den Themen in der folgenden Tabelle beschrieben.
  
|**Thema**|**Beschreibung**|
|:-----|:-----|
|[Ereignisbenachrichtigung in MAPI](event-notification-in-mapi.md) <br/> |Allgemeine Übersicht über die Benachrichtigung und Benachrichtigungsereignisse.  <br/> |
|[Behandeln von Benachrichtigungen](handling-notifications.md) <br/> |Erläuterung der wie Clients Benachrichtigungen behandelt werden sollen.  <br/> |
|[Benachrichtigung bei unterstützenden](supporting-event-notification.md) <br/> |Erläuterung der wie-Dienstanbieter die **IMAPISupport** -Methode verwenden können, um Benachrichtigungen zu generieren.  <br/> |
   
Da Tabelle Benachrichtigungen asynchron sind, können Clients Benachrichtigung über eine hinzugefügte Zeile nach Informationen über das Hinzufügen auf andere Weise erhalten. Es ist möglich, erhalten ein TABLE_ERROR-Ereignis, wenn in einer **IMAPITable::Sort**, **IMAPITable::SetColumns** oder **Methode IMAPITable:: Restrict**-Methode ein Fehler aufgetreten ist, oder wenn eine zugrunde liegende versucht, eine Tabelle mit, aktualisieren, beispielsweise neu oder geänderte Zeilen. 
  
## <a name="see-also"></a>Siehe auch

- [Benachrichtigung](notification.md) 
- [ScDupPropset](scduppropset.md)
- [' Srow '](srow.md)
- [SPropValue](spropvalue.md)
- [MAPI-Strukturen](mapi-structures.md)

