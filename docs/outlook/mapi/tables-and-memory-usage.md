---
title: Tabellen und die Speicherauslastung
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
ms.localizationpriority: medium
api_type:
- COM
ms.assetid: 7ac11e60-6b2c-4241-96e2-20219f84d949
description: 'Letzte Änderung: Samstag, 23. Juli 2011'
ms.openlocfilehash: 7ddb50ba5c64ca91485252c0d58de5d2febf7cd4
ms.sourcegitcommit: a1d9041c20256616c9c183f7d1049142a7ac6991
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 09/24/2021
ms.locfileid: "59566304"
---
# <a name="tables-and-memory-usage"></a>Tabellen und die Speicherauslastung

**Gilt für**: Outlook 2013 | Outlook 2016 
  
Ein wichtiges Problem im Zusammenhang mit dem Abrufen von Daten aus einer Tabelle ist die Speichernutzung. Fehlender Arbeitsspeicher kann dazu [führen, dass IMAPITable::QueryRows](imapitable-queryrows.md) und [HrQueryAllRows](hrqueryallrows.md) fehlschlagen und weniger als die gewünschte Anzahl von Zeilen zurückgegeben wird. Die Entscheidung, welche Methode oder Funktion zum Abrufen von Tabellendaten verwendet werden soll, hängt davon ab, ob davon ausgegangen werden kann, dass die Tabelle in den Arbeitsspeicher passt, und wenn dies nicht möglich ist, ob ein Fehler akzeptabel ist. 
  
Da es nicht immer einfach ist, die Menge der Daten zu ermitteln, die gleichzeitig in den Arbeitsspeicher passen, stellt MAPI einige grundlegende Richtlinien für eine Clientanwendung oder einen Dienstanbieter bereit. Beachten Sie, dass es immer Ausnahmen gibt, basierend auf der jeweiligen Tabellenimplementierungen und der Speicherung der zugrunde liegenden Daten.
  
Die folgenden Richtlinien können verwendet werden, um die Tabellenspeichernutzung auszuwerten:
  
- Clients, die die gelegentliche Speicherauslastung von Arbeitsmappen im Megabyte-Bereich tolerieren können und davon ausgehen können, dass sie keine Probleme beim Lesen einer gesamten Tabelle in den Arbeitsspeicher haben. 
    
- Einschränkungen wirken sich auf die Speicherauslastung einer Tabelle aus. Es kann erwartet werden, dass eine stark eingeschränkte Tabelle mit einer umfangreichen Anzahl von Zeilen, z. B. ein Inhaltsverzeichnis, in den Arbeitsspeicher passt, während eine uneingeschränkte große Tabelle normalerweise nicht möglich ist. 
    
- Mehrere Tabellen im Besitz der MAPI, z. B. Status-, Profil-, Nachrichtendienst-, Anbieter- und Nachrichtenspeichertabellen, passen in der Regel in den Speicher. Dies sind im Allgemeinen kleine Tabellen. Es gibt jedoch Ausnahmen. Beispielsweise kann ein serverbasierter Profilanbieter eine größere Profiltabelle generieren, die nicht passen kann.
    
Um alle Zeilen aus einer Tabelle abzurufen, die ohne Probleme in den Speicher passt, rufen Sie [HrQueryAllRows auf,](hrqueryallrows.md)und legen Sie die maximale Anzahl von Zeilen auf Null fest.
  
Rufen Sie HrQueryAllRows auf, um alle Zeilen aus einer Tabelle abzurufen, die möglicherweise in den Arbeitsspeicher passt oder nicht, indem Sie einen Fehler generieren, indem Sie **HrQueryAllRows** aufrufen, um eine maximale Anzahl von Zeilen anzugeben. Die maximale Anzahl von Zeilen sollte auf eine Zahl festgelegt werden, die größer als die mindeste Anzahl von Zeilen ist, die benötigt werden. Wenn ein Client auf mindestens 50 Zeilen aus einer 300-Zeilentabelle zugreifen muss, sollte die maximale Anzahl von Zeilen auf mindestens 51 festgelegt werden. 
  
Rufen Sie zum Abrufen aller Zeilen aus einer Tabelle, die nicht in den Arbeitsspeicher passen soll, [IMAPITable::QueryRows](imapitable-queryrows.md) in einer Schleife mit einer relativ kleinen Zeilenanzahl auf, wie im folgenden Codebeispiel veranschaulicht: 
  
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

