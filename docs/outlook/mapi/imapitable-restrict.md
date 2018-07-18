---
title: IMAPITableRestrict
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- IMAPITable.Restrict
api_type:
- COM
ms.assetid: a5bfc190-b58f-44c3-893c-8727df14ee58
description: 'Letzte �nderung: Montag, 9. M�rz 2015'
ms.openlocfilehash: 3ab069728f872d82246e8925c5ad35c07f41f02e
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 06/11/2018
ms.locfileid: "19792478"
---
# <a name="imapitablerestrict"></a>IMAPITable::Restrict

  
  
**Betrifft**: Outlook 
  
Wendet einen Filter auf eine Tabelle, reduzieren die Zeile festgelegt, um nur die Zeilen, die den angegebenen Kriterien entsprechen.
  
```cpp
HRESULT Restrict(
LPSRestriction lpRestriction,
ULONG ulFlags
);
```

## <a name="parameters"></a>Parameter

 _lpRestriction_
  
> [in] Zeiger auf eine [SRestriction](srestriction.md) -Struktur, die die Bedingungen des Filters definieren. Übergeben von NULL im Parameter _LpRestriction_ entfernt den aktuellen Filter. 
    
 _ulFlags_
  
> [in] Bitmaske aus Flags, die den Zeitpunkt des Vorgangs Einschränkung steuert. Die folgenden Kennzeichen können festgelegt werden:
    
TBL_ASYNC 
  
> Die Operation asynchron startet und gibt vor dem Abschluss des Vorgangs.
    
TBL_BATCH 
  
> Bewertung des Filters verzögert, bis die Daten in der Tabelle erforderlich ist.
    
## <a name="return-value"></a>R�ckgabewert

S_OK 
  
> Der Filter wurde erfolgreich angewendet.
    
MAPI_E_BUSY 
  
> Ein anderer Vorgang wird ausgeführt, die verhindert, den Einschränkung Vorgang gestartet wird dass. Entweder dürfen der Vorgang in Arbeit abgeschlossen oder angehalten werden sollte.
    
MAPI_E_TOO_COMPLEX 
  
> Die Tabelle kann nicht den Vorgang ausgeführt werden, da der bestimmte Filter auf das durch den Parameter _LpRestriction_ zu kompliziert ist. 
    
## <a name="remarks"></a>Bemerkungen

Die **Methode IMAPITable:: Restrict** -Methode stellt eine Einschränkung oder ein Filter für eine Tabelle her. Wenn eine vorherige Einschränkung vorhanden ist, es verworfen, und die neue Datenbank angewendet. Anwenden einer Einschränkung hat keine Auswirkung auf die zugrunde liegenden Daten einer Tabelle; Diese ändert der Ansicht einfach durch Beschränken der Zeilen, die abgerufen werden können, um Zeilen mit Daten, die die Einschränkung erfüllen. 
  
Es gibt verschiedene Arten von Einschränkungen, jeweils mit einer anderen Struktur beschrieben. Die [SRestriction](srestriction.md) -Datenstruktur enthält zwei Elemente: ein Wert, der den Typ der Einschränkung und die spezifische Struktur für dieses Typs angibt. 
  
Benachrichtigungen für Zeilen der Tabelle, die durch Aufrufe **Restrict** ausgeblendet sind, werden nie generiert. 
  
Eine eigenschaftseinschränkung für eine mehrwertige Eigenschaft funktioniert wie eine Einschränkung für eine einwertige Eigenschaft. Eine mehrwertige Eigenschaft in einer eigenschaftseinschränkung verwendet werden muss die MVI_FLAG gekennzeichnet sind. Wenn dieses Flag festgelegt ist, wird es als ein solcher geordnete Tupel behandelt. Ein Vergleich von zwei mehrwertige Spalten werden die Spalte Elemente in der Reihenfolge, reporting die Beziehung der Spalten auf dem ersten Zeichen verglichen. Gleichheit wird nur zurückgegeben, wenn die Spalten im Vergleich dieselben Werte wie in der gleichen Reihenfolge enthalten. Wenn eine Spalte weniger Werte als die andere verfügt, kann die gemeldete Beziehung, die über einen null-Wert auf den anderen Wert.
  
Weitere Informationen zu Beschränkungen finden Sie unter [Informationen zu Einschränkungen](about-restrictions.md).
  
> [!NOTE]
> Wenn Sie dynamische Abfragen von Daten auf dem Server erstellen, verwenden Sie anstelle der **Restrict** -Methode und die **QueryRows** -Methode zusammen mit **FindRow** -Methode. Die **Restrict** -Methode erstellt eine zwischengespeicherte Ansicht, die verwendet wird, für alle Nachrichten, die in den Basisordner geändert oder hinzugefügt ausgewertet werden soll. Wenn eine Clientanwendung die **Restrict** -Methode für jede dynamische Abfrage verwendet wird, wird eine zwischengespeicherte Ansicht für jede Abfrage erstellt werden. 
  
## <a name="notes-to-callers"></a>Hinweise für Aufrufer

Um der aktuellen Einschränkung verwerfen, ohne einen neuen Anwendungspool erstellen, übergeben Sie NULL _LpRestriction_.
  
Wenn eine andere asynchrone Tabelle Anruf ausgeführt wird, können, auf dem Sie [IMAPITable::Abort](imapitable-abort.md) , um den Anruf zu beenden anrufen **Restrict** zurückzugebenden MAPI_E_BUSY, verursacht. 
  
 **Restrict** arbeitet synchron, es sei denn, Sie eines der Flags festlegen. Wenn Sie das TBL_BATCH-Flag festlegen, verschiebt **Restrict** die Auswertung der Einschränkung, es sei denn, Sie die Daten anfordern. Wenn das Flag TBL_ASYNC festgelegt ist, arbeitet **Restrict**asynchron potenziell vor dem Abschluss des Vorgangs zurückgeben.
  
Wenn **Restrict** wird aufgerufen, und BOOKMARK_CURRENT der aktuellen Cursorposition an den Anfang der Tabelle festgelegt ist, werden alle Textmarken für eine Tabelle verworfen. 
  
Wenn Sie versuchen, eine eigenschaftseinschränkung für eine Eigenschaft zugrunde liegen, die nicht in der Tabelle Spalte Set ist, sind die Ergebnisse nicht definiert. Wenn Sie nicht sicher sind, ob eine Eigenschaft in einer Tabelle unterstützt wird, Kombinieren der eigenschaftseinschränkung mit einer Einschränkung vorhanden. Die Einschränkung überprüft, ob der-Eigenschaft, bevor Sie versuchen, die eigenschaftseinschränkung bedingen vorhanden. 
  
Davon ausgehen, dass eine Benachrichtigung zu erhalten Tabelle in einer Zeile, die gefiltert wurde aus einer Tabelle aufgrund einer Einschränkung.
  
## <a name="mfcmapi-reference"></a>MFCMAPI (engl.) (engl.)

Beispielcode MFCMAPI (engl.) finden Sie in der folgenden Tabelle.
  
|**Datei**|**Funktion**|**Comment**|
|:-----|:-----|:-----|
|ContentsTableListCtrl.cpp  <br/> |CContentsTableListCtrl::ApplyRestriction  <br/> |MFCMAPI (engl.) verwendet die **Methode IMAPITable:: Restrict** -Methode, um eine Einschränkung für eine Tabelle festgelegt.  <br/> |
   
## <a name="see-also"></a>Siehe auch



[IMAPITable::Abort](imapitable-abort.md)
  
[IMAPITable::FindRow](imapitable-findrow.md)
  
[IMAPITable::GetRowCount](imapitable-getrowcount.md)
  
[IMAPITable::QueryRows](imapitable-queryrows.md)
  
[SPropertyRestriction](spropertyrestriction.md)
  
[IMAPITable : IUnknown](imapitableiunknown.md)


[MFCMAPI (engl.) als ein Codebeispiel](mfcmapi-as-a-code-sample.md)

