---
title: Tabellen und die Speicherauslastung
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
localization_priority: Normal
api_type:
- COM
ms.assetid: 7ac11e60-6b2c-4241-96e2-20219f84d949
description: 'Letzte Änderung: Samstag, 23. Juli 2011'
ms.openlocfilehash: afd69f5a3fff69f670d6be78ba4957307cdb6995
ms.sourcegitcommit: 8657170d071f9bcf680aba50b9c07f2a4fb82283
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 04/28/2019
ms.locfileid: "33436860"
---
# <a name="tables-and-memory-usage"></a>Tabellen und die Speicherauslastung

**Gilt für**: Outlook 2013 | Outlook 2016 
  
Ein wichtiges Problem im Zusammenhang mit dem Abrufen von Daten aus einer Tabelle ist die Speichernutzung. Fehlender verfügbarer Arbeitsspeicher kann dazu führen, dass [IMAPITable::QueryRows](imapitable-queryrows.md) und [HrQueryAllRows](hrqueryallrows.md) fehlschlagen und weniger als die gewünschte Anzahl von Zeilen zurückgegeben werden. Die Entscheidung, welche Methode oder Funktion zum Abrufen von Tabellendaten verwendet werden soll, hängt davon ab, ob erwartet werden kann, dass die Tabelle in den Arbeitsspeicher passt, und ob dies nicht möglich ist, wenn ein Fehler akzeptabel ist. 
  
Da es nicht immer einfach ist, die Datenmenge zu bestimmen, die gleichzeitig in den Arbeitsspeicher passt, bietet MAPI einige grundlegende Richtlinien für eine Clientanwendung oder einen Dienstanbieter, die folgen sollen. Denken Sie daran, dass es immer Ausnahmen gibt, basierend auf der jeweiligen Tabellenimplementierung und der Art und Weise, wie die zugrunde liegenden Daten gespeichert werden.
  
Die folgenden Richtlinien können verwendet werden, um die Verwendung des Tabellenspeichers auszuwerten:
  
- Clients, die gelegentliche Arbeitsspeicherauslastungen im Megabytebereich tolerieren können und davon ausgehen können, dass sie keine Probleme haben, eine gesamte Tabelle in den Arbeitsspeicher zu lesen. 
    
- Einschränkungen haben Auswirkungen auf die Verwendung des Arbeitsspeichers in einer Tabelle. Es ist zu erwarten, dass eine stark eingeschränkte Tabelle mit einer großen Anzahl von Zeilen, z. B. einer Inhaltstabelle, in den Arbeitsspeicher passt, während eine unbeschränkte große Tabelle in der Regel nicht möglich ist. 
    
- Einige der Tabellen im Besitz von MAPI, z. B. Status-, Profil-, Nachrichtendienst-, Anbieter- und Nachrichtenspeichertabellen, passen in der Regel in den Arbeitsspeicher. Dies sind im Allgemeinen kleine Tabellen. Es gibt jedoch Ausnahmen. Beispielsweise kann ein serverbasierter Profilanbieter eine größere Profiltabelle generieren, die nicht passen kann.
    
Um alle Zeilen aus einer Tabelle abzurufen, die problemlos in den Arbeitsspeicher passt, rufen Sie [HrQueryAllRows](hrqueryallrows.md)auf, und legen Sie die maximale Anzahl von Zeilen auf Null fest.
  
Um alle Zeilen aus einer Tabelle abzurufen, die möglicherweise nicht in den Arbeitsspeicher passt, wird ein Fehler generiert, indem **Sie HrQueryAllRows** aufrufen, um eine maximale Anzahl von Zeilen anzugeben. Die maximale Anzahl von Zeilen sollte auf eine Zahl festgelegt werden, die größer als die mindestanzahl der erforderlichen Zeilen ist. Wenn ein Client aus einer 300-Zeilentabelle auf mindestens 50 Zeilen zugreifen muss, sollte die maximale Anzahl von Zeilen auf mindestens 51 festgelegt werden. 
  
Um alle Zeilen aus einer Tabelle abzurufen, die nicht in den Arbeitsspeicher passen soll, rufen Sie [IMAPITable::QueryRows](imapitable-queryrows.md) in einer Schleife mit einer relativ kleinen Zeilenanzahl auf, wie im folgenden Codebeispiel veranschaulicht wird: 
  
```cpp
HRESULT     hr;
LPSRowSet   pRows = NULL;
LONG        irow;
LONG            cAsk = 50;                  // adjust this value
while ((hr = pTable->QueryRows(cAsk, 0, &pRows)) == hrSuccess
        && pRows->cRows != 0)
{
    for (irow = 0; irow < prows->cRows; ++irow)
    {
        // process the row...
    }
    FreeProws(pRows);
    pRows = NULL;
}
if (hr)
{
    // handle the error...
}
 
```

Wenn diese Schleife abgeschlossen ist und alle Zeilen in der Tabelle verarbeitet wurden und  _cRows_ null ist, befindet sich die Position des Cursors in der Regel am unteren Rand der Tabelle. 
  
## <a name="see-also"></a>Siehe auch

- [MAPI-Tabellen](mapi-tables.md)

