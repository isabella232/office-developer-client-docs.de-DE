---
title: IMAPITableRestrict
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
ms.localizationpriority: medium
api_name:
- IMAPITable.Restrict
api_type:
- COM
ms.assetid: a5bfc190-b58f-44c3-893c-8727df14ee58
description: 'Letzte Änderung: Montag, 9. März 2015'
ms.openlocfilehash: 0b13d12d78d9b24174d708778648040b67f69da8
ms.sourcegitcommit: a1d9041c20256616c9c183f7d1049142a7ac6991
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 09/24/2021
ms.locfileid: "59600869"
---
# <a name="imapitablerestrict"></a>IMAPITable::Restrict

  
  
**Gilt für**: Outlook 2013 | Outlook 2016 
  
Wendet einen Filter auf eine Tabelle an, wodurch der Zeilensatz auf die Zeilen reduziert wird, die den angegebenen Kriterien entsprechen.
  
```cpp
HRESULT Restrict(
LPSRestriction lpRestriction,
ULONG ulFlags
);
```

## <a name="parameters"></a>Parameter

 _lpRestriction_
  
> [in] Zeiger auf eine [SRestriction-Struktur,](srestriction.md) die die Bedingungen des Filters definiert. Durch Übergeben von NULL im  _lpRestriction-Parameter_ wird der aktuelle Filter entfernt. 
    
 _ulFlags_
  
> [in] Bitmaske von Flags, die den Zeitpunkt des Einschränkungsvorgangs steuert. Die folgenden Flags können festgelegt werden:
    
TBL_ASYNC 
  
> Startet den Vorgang asynchron und gibt zurück, bevor der Vorgang abgeschlossen wird.
    
TBL_BATCH 
  
> Verzögert die Auswertung des Filters, bis die Daten in der Tabelle erforderlich sind.
    
## <a name="return-value"></a>Rückgabewert

S_OK 
  
> Der Filter wurde erfolgreich angewendet.
    
MAPI_E_BUSY 
  
> Ein weiterer Vorgang wird ausgeführt, der verhindert, dass der Einschränkungsvorgang gestartet wird. Entweder sollte der laufende Vorgang abgeschlossen werden können, oder er sollte beendet werden.
    
MAPI_E_TOO_COMPLEX 
  
> Die Tabelle kann den Vorgang nicht ausführen, da der bestimmte Filter, auf den der  _parameter lpRestriction_ verweist, zu kompliziert ist. 
    
## <a name="remarks"></a>HinwBemerkungeneise

Die **IMAPITable::Restrict-Methode** richtet eine Einschränkung oder einen Filter für eine Tabelle ein. Wenn eine vorherige Einschränkung vorliegt, wird sie verworfen und die neue angewendet. Das Anwenden einer Einschränkung hat keine Auswirkungen auf die zugrunde liegenden Daten einer Tabelle. Sie ändert einfach die Ansicht, indem die abzurufenden Zeilen auf Zeilen beschränkt werden, die Daten enthalten, die die Einschränkung erfüllen. 
  
Es gibt verschiedene Arten von Einschränkungen, die jeweils mit einer anderen Struktur beschrieben werden. Die [SRestriction-Struktur](srestriction.md) enthält zwei Elemente: einen Wert, der den Typ der Einschränkung und die spezifische Struktur angibt, die für diesen Typ anwendbar ist. 
  
Benachrichtigungen für Tabellenzeilen, die durch Aufrufe der **Einschränkung** aus der Ansicht ausgeblendet werden, werden nie generiert. 
  
Eine Eigenschaftseinschränkung für eine mehrwertige Eigenschaft funktioniert wie eine Einschränkung für eine einwertige Eigenschaft. Für eine mehrwertige Eigenschaft, die in einer Eigenschaftseinschränkung verwendet werden soll, muss das MVI_FLAG Flag festgelegt sein. Wenn dieses Kennzeichen nicht festgelegt ist, wird es als vollständig sortiertes Tupel behandelt. Bei einem Vergleich von zwei mehrwertigen Spalten werden die Spaltenelemente in der reihenfolge verglichen, wobei die Beziehung der Spalten bei der ersten Gleichung gemeldet wird. Gleichheit wird nur zurückgegeben, wenn die verglichenen Spalten dieselben Werte in derselben Reihenfolge enthalten. Wenn eine Spalte weniger Werte aufweist als die andere, ist die gemeldete Beziehung die eines NULL-Werts zum anderen Wert.
  
Weitere Informationen zu Einschränkungen finden Sie unter ["Einschränkungen".](about-restrictions.md)
  
> [!NOTE]
> Wenn Sie dynamische Abfragen erstellen, um nach Daten auf dem Server zu suchen, verwenden Sie die **FindRow-Methode,** anstatt die **Restrict-Methode** und die **QueryRows-Methode** zusammen zu verwenden. Die **Restrict-Methode** erstellt eine zwischengespeicherte Ansicht, die verwendet wird, um alle Nachrichten auszuwerten, die dem Basisordner hinzugefügt oder geändert wurden. Wenn eine Clientanwendung die **Restrict-Methode** für jede dynamische Abfrage verwendet, wird für jede Abfrage eine zwischengespeicherte Ansicht erstellt. 
  
## <a name="notes-to-callers"></a>Hinweise für Aufrufer

Übergeben Sie NULL in  _lpRestriction,_ um die aktuelle Einschränkung zu verwerfen, ohne eine neue zu erstellen.
  
Wenn ein weiterer asynchroner Tabellenaufruf ausgeführt wird, wodurch **Restrict** MAPI_E_BUSY zurückgibt, können Sie [IMAPITable::Abort](imapitable-abort.md) aufrufen, um den Aufruf zu beenden. 
  
 **Die Einschränkung** wird synchron ausgeführt, es sei denn, Sie legen eines der Flags fest. Wenn Sie das flag TBL_BATCH festlegen, verschiebt **Restrict** die Auswertung der Einschränkung, es sei denn, Sie fordern die Daten an. Wenn das flag TBL_ASYNC festgelegt ist, wird **Restrict** asynchron ausgeführt und wird möglicherweise vor Abschluss des Vorgangs zurückgegeben.
  
Alle Textmarken für eine Tabelle werden verworfen, wenn ein Aufruf von **Restrict** ausgeführt wird, und BOOKMARK_CURRENT, die aktuelle Cursorposition, auf den Anfang der Tabelle festgelegt wird. 
  
Wenn Sie versuchen, eine Eigenschaftseinschränkung für eine Eigenschaft festzulegen, die nicht im Spaltensatz der Tabelle enthalten ist, sind die Ergebnisse nicht definiert. Wenn Sie sich nicht sicher sind, ob eine Eigenschaft in einer Tabelle unterstützt wird, kombinieren Sie die Eigenschaftseinschränkung mit einer vorhandenen Einschränkung. Die vorhandene Einschränkung prüft, ob die Eigenschaft vorhanden ist, bevor versucht wird, die Eigenschaftseinschränkung aufzuerlegen. 
  
Gehen Sie nicht davon aus, eine Tabellenbenachrichtigung in einer Zeile zu erhalten, die aufgrund einer Einschränkung aus einer Tabelle gefiltert wurde.
  
## <a name="mfcmapi-reference"></a>MFCMAPI-Referenz

Einen MFCMAP-Beispielcode finden Sie in der folgenden Tabelle.
  
|**Datei**|**Funktion**|**Comment**|
|:-----|:-----|:-----|
|ContentsTableListCtrl.cpp  <br/> |CContentsTableListCtrl::ApplyRestriction  <br/> |MFCMAPI verwendet die **IMAPITable::Restrict-Methode,** um eine Einschränkung für eine Tabelle festzulegen.  <br/> |
   
## <a name="see-also"></a>Siehe auch



[IMAPITable::Abort](imapitable-abort.md)
  
[IMAPITable::FindRow](imapitable-findrow.md)
  
[IMAPITable::GetRowCount](imapitable-getrowcount.md)
  
[IMAPITable::QueryRows](imapitable-queryrows.md)
  
[SPropertyRestriction](spropertyrestriction.md)
  
[IMAPITable : IUnknown](imapitableiunknown.md)


[MFCMAPI (engl.) als ein Codebeispiel](mfcmapi-as-a-code-sample.md)

