---
title: Tabellen und Speicherverwendung
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
localization_priority: Normal
api_type:
- COM
ms.assetid: 7ac11e60-6b2c-4241-96e2-20219f84d949
description: 'Letzte �nderung: Samstag, 23. Juli 2011'
ms.openlocfilehash: 390cec0cc59f189f83af2c5339512d82e125771e
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 06/11/2018
ms.locfileid: "19795718"
---
# <a name="tables-and-memory-usage"></a>Tabellen und Speicherverwendung

**Betrifft**: Outlook 
  
Ein wichtiger Aspekt beim Abrufen von Daten aus einer Tabelle verbunden ist, die Speicherverwendung. Wenig verfügbarer Arbeitsspeicher kann [IMAPITable::QueryRows](imapitable-queryrows.md) und [HrQueryAllRows](hrqueryallrows.md) ein Fehler auftritt, kleiner als die gewünschte Anzahl von Zeilen zurückgeben. Entscheiden, welche Methode oder der Funktion zum Abrufen von Tabellendaten hängt davon ab, ob die Tabelle im Arbeitsspeicher passt erwartet werden kann, und ist es nicht möglich, wenn Fehler zulässig ist. 
  
Da nicht immer leicht um die Menge der Daten zu ermitteln, die gleichzeitig in den Arbeitsspeicher passt, bietet MAPI einige grundlegenden Richtlinien für eine Clientanwendung oder Dienstanbieter, denen Sie folgen. Denken Sie daran, dass es sind immer Ausnahmen, basierend auf die bestimmte Tabelle Implementierung und wie die zugrunde liegenden Daten gespeichert werden.
  
Die folgenden Richtlinien können verwendet werden, für die Speicherverwendung Tabelle ausgewertet werden soll:
  
- Clients, die gelegentlich Working Set Speicherverwendung im Bereich Megabyte tolerieren können und können davon werden keine Probleme, die eine ganze Tabelle in den Arbeitsspeicher gelesen haben. 
    
- Einschränkungen haben einen Einfluss auf eine Tabelle Verwendung des Arbeitsspeichers. Eine stark eingeschränkte Tabelle mit einer umfangreichen Anzahl von Zeilen, wie etwa eine Inhaltstabelle kann in den Arbeitsspeicher angepasst wird, während eine uneingeschränkte große Tabelle in der Regel nicht erwartet. 
    
- Einige der Tabellen Besitz MAPI wie Status, Profil, Messagingdiensts, Anbieter und Nachricht Store Tabellen, werden in der Regel im Arbeitsspeicher passen. Dies sind im Allgemeinen kleine Tabellen. Es gibt jedoch Ausnahmen. Beispielsweise kann ein serverbasiertes Profilanbieter eine größere Profiltabelle generieren, die nicht angepasst werden können.
    
Rufen Sie auf, um alle Zeilen aus einer Tabelle abzurufen, die in den Arbeitsspeicher ohne Probleme passt, [HrQueryAllRows](hrqueryallrows.md), wenn die maximale Anzahl von Zeilen auf 0 (null) festlegen.
  
Rufen Sie zum Abrufen aller Zeilen aus einer Tabelle, die möglicherweise nicht in den Arbeitsspeicher, ein Fehler generiert wird passt, **HrQueryAllRows** eine maximale Anzahl von Zeilen angeben. Die maximale Anzahl von Zeilen sollte auf eine Zahl größer als die minimale Anzahl von Zeilen festgelegt werden, die erforderlich sind. Wenn ein Client mindestens 50 Zeilen aus einer Tabelle 300 Zeile zugreifen muss, sollte die maximale Anzahl der Zeilen auf mindestens 51 festgelegt werden. 
  
Rufen Sie alle Zeilen aus einer Tabelle, die möglicherweise nicht in den Speicher passen rufen Sie [IMAPITable::QueryRows](imapitable-queryrows.md) in einer Schleife mit relativ geringe Zeilenanzahl auf, wie im folgenden Codebeispiel veranschaulicht wird: 
  
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

Wenn diese Schleife abgeschlossen ist und alle Zeilen in der Tabelle verarbeitet wurden und _cRows_ NULL ist, werden die Position des Cursors in der Regel am unteren Rand der Tabelle. 
  
## <a name="see-also"></a>Siehe auch

- [MAPI-Tabellen](mapi-tables.md)

