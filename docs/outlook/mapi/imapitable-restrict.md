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
ms.openlocfilehash: 6cca6bc12fa6f100885b7bf705d79fa24a2e2f91
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 04/23/2019
ms.locfileid: "32328847"
---
# <a name="imapitablerestrict"></a>IMAPITable::Restrict

  
  
**Gilt für**: Outlook 2013 | Outlook 2016 
  
Wendet einen Filter auf eine Tabelle an, wobei der Zeilensatz nur auf die Zeilen reduziert wird, die den angegebenen Kriterien entsprechen.
  
```cpp
HRESULT Restrict(
LPSRestriction lpRestriction,
ULONG ulFlags
);
```

## <a name="parameters"></a>Parameter

 _lpRestriction_
  
> in Zeiger auf eine [SRestriction](srestriction.md) -Struktur, die die Bedingungen des Filters definiert. Durch das Übergeben von NULL im _lpRestriction_ -Parameter wird der aktuelle Filter entfernt. 
    
 _ulFlags_
  
> in Bitmaske von Flags, die das Timing des Einschränkungs Vorgangs steuert. Die folgenden Flags können festgelegt werden:
    
TBL_ASYNC 
  
> Startet den Vorgang asynchron und gibt vor dem Abschluss des Vorgangs zurück.
    
TBL_BATCH 
  
> Verzögert die Auswertung des Filters, bis die Daten in der Tabelle erforderlich sind.
    
## <a name="return-value"></a>Rückgabewert

S_OK 
  
> Der Filter wurde erfolgreich angewendet.
    
MAPI_E_BUSY 
  
> Ein anderer Vorgang wird ausgeführt, der verhindert, dass der Einschränkungs Vorgang gestartet wird. Entweder sollte der ausgeführte Vorgang abgeschlossen oder beendet werden.
    
MAPI_E_TOO_COMPLEX 
  
> Die Tabelle kann den Vorgang nicht ausführen, da der bestimmte Filter, auf den durch den _lpRestriction_ -Parameter verwiesen wird, zu kompliziert ist. 
    
## <a name="remarks"></a>Bemerkungen

Die **IMAPITable:: Restrict** -Methode richtet eine Einschränkung oder einen Filter für eine Tabelle ein. Wenn es eine frühere Einschränkung gibt, wird sie verworfen und die neue angewendet. Das Anwenden einer Einschränkung hat keine Auswirkungen auf die zugrunde liegenden Daten einer Tabelle; Es ändert lediglich die Ansicht, indem die Zeilen eingeschränkt werden, die in Zeilen mit Daten abgerufen werden können, die die Einschränkung erfüllen. 
  
Es gibt verschiedene Arten von Einschränkungen, die jeweils mit einer anderen Struktur beschrieben werden. Die [SRestriction](srestriction.md) -Struktur enthält zwei Elemente: ein Wert, der den Typ der Einschränkung und die spezifische Struktur angibt, die für diesen Typ gilt. 
  
Benachrichtigungen für Tabellenzeilen, die durch Aufrufe von **Restrict** ausgeblendet werden, werden nie generiert. 
  
Eine Eigenschaftseinschränkung für eine mehrwertige Eigenschaft funktioniert wie eine Einschränkung für eine einwertige Eigenschaft. Für eine mehrwertige Eigenschaft, die in einer Eigenschaftseinschränkung verwendet werden soll, muss das MVI_FLAG-Flag festgelegt sein. Wenn dieses Flag nicht festgelegt ist, wird es als vollständig geordnetes Tupel behandelt. Bei einem Vergleich zwischen zwei mehrwertigen Spalten werden die Spaltenelemente in der Reihenfolge verglichen, wobei die Relation der Spalten bei der ersten Ungleichung gemeldet wird. Gleichheit wird nur zurückgegeben, wenn die verglichenen Spalten die gleichen Werte in derselben Reihenfolge enthalten. Wenn eine Spalte weniger Werte als die andere hat, ist die berichtete Relation die eines NULL-Werts für den anderen Wert.
  
Weitere Informationen zu Einschränkungen finden Sie unter [Informationen zu Einschränkungen](about-restrictions.md).
  
> [!NOTE]
> Wenn Sie dynamische Abfragen zum Suchen nach Daten auf dem Server erstellen, verwenden Sie die **FindRow** -Methode, anstatt die **Restrict** -Methode und die **QueryRows** -Methode zusammen zu verwenden. Die **Restrict** -Methode erstellt eine zwischengespeicherte Ansicht, die zum Auswerten aller Nachrichten verwendet wird, die im Basisordner hinzugefügt oder geändert wurden. Wenn eine Clientanwendung die **Restrict** -Methode für jede dynamische Abfrage verwendet, wird für jede Abfrage eine zwischengespeicherte Ansicht erstellt. 
  
## <a name="notes-to-callers"></a>Hinweise für Aufrufer

Um die aktuelle Einschränkung zu verwerfen, ohne eine neue zu erstellen, müssen Sie in _lpRestriction_den Wert NULL überschreiten.
  
Wenn ein anderer asynchroner Tabellen Aufruf ausgeführt wird, wodurch **Restrict** MAPI_E_BUSY zurückgegeben wird, können Sie [IMAPITable:: Abort](imapitable-abort.md) aufrufen, um den Anruf zu beenden. 
  
 **Restrict** arbeitet synchron, es sei denn, Sie legen eine der Flags fest. Wenn Sie das TBL_BATCH-Flag festlegen, verschiebt **Restrict** die Bewertung der Einschränkung, es sei denn, Sie fordern die Daten an. Wenn das TBL_ASYNC-Flag festgelegt ist, wird **Restrict**asynchron ausgeführt, was möglicherweise vor dem Abschluss des Vorgangs zurückgegeben wird.
  
Alle Lesezeichen für eine Tabelle werden verworfen, wenn ein Aufruf von **Restrict** ausgeführt wird und BOOKMARK_CURRENT, die aktuelle Cursorposition, auf den Anfang der Tabelle festgelegt ist. 
  
Wenn Sie versuchen, eine Eigenschaftseinschränkung für eine Eigenschaft aufzuerlegen, die nicht im Spaltensatz der Tabelle enthalten ist, sind die Ergebnisse nicht definiert. Wenn Sie nicht sicher sind, ob eine Eigenschaft in einer Tabelle unterstützt wird, kombinieren Sie die Eigenschaftseinschränkung mit einer EXISTS-Einschränkung. Die EXISTS-Einschränkung überprüft, ob die Eigenschaft vorhanden ist, bevor Sie versuchen, die Eigenschaftseinschränkung aufzuzwingen. 
  
Erwarten Sie nicht, dass Sie eine Tabellenbenachrichtigung für eine Zeile erhalten, die aufgrund einer Einschränkung aus einer Tabelle gefiltert wurde.
  
## <a name="mfcmapi-reference"></a>MFCMAPI-Referenz

Einen MFCMAP-Beispielcode finden Sie in der folgenden Tabelle.
  
|**Datei**|**Funktion**|**Comment**|
|:-----|:-----|:-----|
|ContentsTableListCtrl. cpp  <br/> |CContentsTableListCtrl:: ApplyRestriction  <br/> |MFCMAPI verwendet die **IMAPITable:: Restrict** -Methode, um eine Einschränkung für eine Tabelle festzulegen.  <br/> |
   
## <a name="see-also"></a>Siehe auch



[IMAPITable::Abort](imapitable-abort.md)
  
[IMAPITable::FindRow](imapitable-findrow.md)
  
[IMAPITable::GetRowCount](imapitable-getrowcount.md)
  
[IMAPITable::QueryRows](imapitable-queryrows.md)
  
[SPropertyRestriction](spropertyrestriction.md)
  
[IMAPITable : IUnknown](imapitableiunknown.md)


[MFCMAPI (engl.) als ein Codebeispiel](mfcmapi-as-a-code-sample.md)

