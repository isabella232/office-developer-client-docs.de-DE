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
description: 'Letzte Änderung: Montag, 9. März 2015'
ms.openlocfilehash: 6cca6bc12fa6f100885b7bf705d79fa24a2e2f91
ms.sourcegitcommit: 8657170d071f9bcf680aba50b9c07f2a4fb82283
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 04/28/2019
ms.locfileid: "33414620"
---
# <a name="imapitablerestrict"></a>IMAPITable::Restrict

  
  
**Gilt für**: Outlook 2013 | Outlook 2016 
  
Wendet einen Filter auf eine Tabelle an, wodurch der Zeilensatz auf nur die Zeilen reduziert wird, die den angegebenen Kriterien entsprechen.
  
```cpp
HRESULT Restrict(
LPSRestriction lpRestriction,
ULONG ulFlags
);
```

## <a name="parameters"></a>Parameter

 _lpRestriction_
  
> [in] Zeiger auf eine [SRestriction-Struktur,](srestriction.md) die die Bedingungen des Filters definiert. Durch übergeben von NULL im  _lpRestriction-Parameter_ wird der aktuelle Filter entfernt. 
    
 _ulFlags_
  
> [in] Bitmaske von Flags, die das Timing des Einschränkungsvorgangs steuert. Die folgenden Kennzeichen können festgelegt werden:
    
TBL_ASYNC 
  
> Startet den Vorgang asynchron und gibt zurück, bevor der Vorgang abgeschlossen wird.
    
TBL_BATCH 
  
> Die Auswertung des Filters wird so lange verf?en, bis die Daten in der Tabelle erforderlich sind.
    
## <a name="return-value"></a>Rückgabewert

S_OK 
  
> Der Filter wurde erfolgreich angewendet.
    
MAPI_E_BUSY 
  
> Ein weiterer Vorgang wird ausgeführt, der verhindert, dass der Einschränkungsvorgang gestartet wird. Der ausgeführte Vorgang sollte entweder abgeschlossen oder beendet werden.
    
MAPI_E_TOO_COMPLEX 
  
> Die Tabelle kann den Vorgang nicht ausführen, da der bestimmte Filter, auf den der  _lpRestriction-Parameter_ verweist, zu kompliziert ist. 
    
## <a name="remarks"></a>Hinweise

Die **IMAPITable::Restrict-Methode** richtet eine Einschränkung oder einen Filter für eine Tabelle ein. Wenn es eine vorherige Einschränkung gibt, wird sie verworfen und die neue angewendet. Das Anwenden einer Einschränkung hat keine Auswirkungen auf die zugrunde liegenden Daten einer Tabelle. Es ändert einfach die Ansicht, indem die Zeilen, die abgerufen werden können, auf Zeilen mit Daten begrenzt werden, die die Einschränkung erfüllen. 
  
Es gibt verschiedene Arten von Einschränkungen, die jeweils mit einer anderen Struktur beschrieben werden. Die [SRestriction-Struktur](srestriction.md) enthält zwei Elemente: einen Wert, der den Typ der Einschränkung und die spezifische Struktur angibt, die für diesen Typ gilt. 
  
Benachrichtigungen für Tabellenzeilen, die durch Aufrufe von Restrict aus der Ansicht ausgeblendet **werden,** werden nie generiert. 
  
Eine Eigenschaftseinschränkung für eine mehrwertige Eigenschaft funktioniert wie eine Einschränkung für eine einwertige Eigenschaft. Für eine mehrwertige Eigenschaft, die in einer Eigenschaftseinschränkung verwendet werden soll, muss MVI_FLAG festgelegt sein. Wenn dieses Flag nicht festgelegt ist, wird es als vollständig geordnetes Tupel behandelt. Bei einem Vergleich von zwei mehrwertigen Spalten werden die Spaltenelemente in der Reihenfolge verglichen und das Verhältnis der Spalten bei der ersten Ungleichung angezeigt. Gleichheit wird nur zurückgegeben, wenn die verglichenen Spalten dieselben Werte in derselben Reihenfolge enthalten. Wenn eine Spalte weniger Werte als die andere hat, ist die gemeldete Beziehung die eines Nullwerts zum anderen Wert.
  
Weitere Informationen zu Einschränkungen finden Sie unter [Informationen zu Einschränkungen](about-restrictions.md).
  
> [!NOTE]
> Wenn Sie dynamische Abfragen zum Suchen nach Daten auf dem Server erstellen, verwenden Sie die **FindRow-Methode,** anstatt die **Restrict-Methode** und die **QueryRows-Methode** zusammen zu verwenden. Die **Restrict-Methode** erstellt eine zwischengespeicherte Ansicht, die zum Auswerten aller Nachrichten verwendet wird, die dem Basisordner hinzugefügt oder geändert wurden. Wenn eine Clientanwendung die **Restrict-Methode** für jede dynamische Abfrage verwendet, wird für jede Abfrage eine zwischengespeicherte Ansicht erstellt. 
  
## <a name="notes-to-callers"></a>Hinweise für Aufrufer

Um die aktuelle Einschränkung zu verwerfen, ohne eine neue zu erstellen, übergeben Sie NULL in  _lpRestriction_.
  
Wenn ein weiterer asynchroner Tabellenaufruf ausgeführt wird, wodurch **Restrict** MAPI_E_BUSY zurück gibt, können Sie [IMAPITable::Abort](imapitable-abort.md) aufrufen, um den Anruf zu beenden. 
  
 **Restrict** wird synchron ausgeführt, es sei denn, Sie legen eines der Flags ein. Wenn Sie das TBL_BATCH festlegen, verschiebt **Restrict** die Auswertung der Einschränkung, es sei denn, Sie fordern die Daten an. Wenn das TBL_ASYNC festgelegt ist, wird **Restrict** asynchron betrieben und möglicherweise vor Abschluss des Vorgangs zurückgeben.
  
Alle Lesezeichen für eine Tabelle werden verworfen, wenn ein Aufruf von **Restrict** erfolgt, und BOOKMARK_CURRENT, die aktuelle Cursorposition, wird auf den Anfang der Tabelle festgelegt. 
  
Wenn Sie versuchen, einer Eigenschaft, die nicht im Spaltensatz der Tabelle enthalten ist, eine Eigenschaftseinschränkung aufzuerzwingen, sind die Ergebnisse nicht definiert. Wenn Sie nicht sicher sind, ob eine Eigenschaft in einer Tabelle unterstützt wird, kombinieren Sie die Eigenschaftseinschränkung mit einer vorhandenen Einschränkung. Mit der vorhandenen Einschränkung wird überprüft, ob die Eigenschaft vorhanden ist, bevor versucht wird, die Eigenschaftseinschränkung zu verhängen. 
  
Erwarten Sie keine Tabellenbenachrichtigung für eine Zeile, die aufgrund einer Einschränkung aus einer Tabelle gefiltert wurde.
  
## <a name="mfcmapi-reference"></a>MFCMAPI-Referenz

Einen MFCMAP-Beispielcode finden Sie in der folgenden Tabelle.
  
|**Datei**|**Funktion**|**Comment**|
|:-----|:-----|:-----|
|ContentsTableListCtrl.cpp  <br/> |CContentsTableListCtrl::ApplyRestriction  <br/> |MFCMAPI verwendet die **IMAPITable::Restrict-Methode,** um eine Einschränkung für eine Tabelle festlegen.  <br/> |
   
## <a name="see-also"></a>Siehe auch



[IMAPITable::Abort](imapitable-abort.md)
  
[IMAPITable::FindRow](imapitable-findrow.md)
  
[IMAPITable::GetRowCount](imapitable-getrowcount.md)
  
[IMAPITable::QueryRows](imapitable-queryrows.md)
  
[SPropertyRestriction](spropertyrestriction.md)
  
[IMAPITable : IUnknown](imapitableiunknown.md)


[MFCMAPI (engl.) als ein Codebeispiel](mfcmapi-as-a-code-sample.md)

