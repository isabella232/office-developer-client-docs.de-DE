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
  
Ein wichtiges Problem beim Abrufen von Daten aus einer Tabelle ist die Speicherauslastung. Fehlender verfügbarer Arbeitsspeicher kann dazu führen, dass [IMAPITable:: QueryRows](imapitable-queryrows.md) und [HrQueryAllRows](hrqueryallrows.md) fehlschlägt, sodass weniger als die gewünschte Anzahl von Zeilen zurückgegeben wird. Die Entscheidung, welche Methode oder Funktion zum Abrufen von Tabellendaten verwendet werden kann, hängt davon ab, ob die Tabelle in den Arbeitsspeicher passt, und falls dies nicht möglich ist, wenn ein Fehlschlagen akzeptabel ist. 
  
Da es nicht immer einfach ist, die Datenmenge zu bestimmen, die gleichzeitig in den Arbeitsspeicher passt, bietet MAPI einige grundlegende Richtlinien für eine Clientanwendung oder einen Dienstanbieter. Denken Sie daran, dass es immer Ausnahmen gibt, die auf der jeweiligen Tabellen Implementierung basieren und wie die zugrunde liegenden Daten gespeichert werden.
  
Die folgenden Richtlinien können zum Auswerten der Tabellenspeicher Verwendung verwendet werden:
  
- Clients, die gelegentlich Arbeitsspeicherauslastung im megabytebereich tolerieren können und davon ausgehen, dass Sie keine Probleme beim Lesen einer gesamten Tabelle in den Arbeitsspeicher haben. 
    
- Einschränkungen wirken sich auf die Speicherbelegung einer Tabelle aus. Eine stark eingeschränkte Tabelle mit einer umfangreichen Anzahl von Zeilen, wie etwa einer Inhaltstabelle, kann voraussichtlich in den Arbeitsspeicher integriert werden, während eine uneingeschränkte große Tabelle in der Regel nicht möglich ist. 
    
- Einige der Tabellen, die MAPI gehören, wie Status-, Profil-, Nachrichtendienst-, Anbieter-und nachrichtenspeichertabellen, werden in der Regel in den Arbeitsspeicher passt. Hierbei handelt es sich im Allgemeinen um kleine Tabellen. Es gibt jedoch Ausnahmen. Ein serverbasierter Profilanbieter kann beispielsweise eine größere Profiltabelle generieren, die nicht angepasst werden kann.
    
Wenn Sie alle Zeilen aus einer Tabelle abrufen möchten, die ohne Probleme in den Arbeitsspeicher passt, rufen Sie [HrQueryAllRows](hrqueryallrows.md)auf, und legen Sie die maximale Anzahl von Zeilen auf NULL fest.
  
Wenn Sie alle Zeilen aus einer Tabelle abrufen möchten, die möglicherweise nicht in den Arbeitsspeicher passt, und einen Fehler generiert, rufen Sie **HrQueryAllRows** auf, um eine maximale Anzahl von Zeilen anzugeben. Die maximale Anzahl von Zeilen sollte auf eine Zahl festgelegt werden, die größer ist als die Mindestanzahl der benötigten Zeilen. Wenn ein Client auf mindestens 50 Zeilen aus einer 300-Zeilentabelle zugreifen muss, sollte die maximale Anzahl von Zeilen auf mindestens 51 festgelegt werden. 
  
Wenn Sie alle Zeilen aus einer Tabelle abrufen möchten, die nicht in den Arbeitsspeicher passt, rufen Sie [IMAPITable:: QueryRows](imapitable-queryrows.md) in einer Schleife mit einer relativ kleinen Zeilenanzahl auf, wie im folgenden Codebeispiel veranschaulicht: 
  
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

Wenn diese Schleife abgeschlossen ist und alle Zeilen in der Tabelle verarbeitet wurden und _Crows_ gleich NULL ist, wird die Position des Cursors in der Regel am unteren Rand der Tabelle angezeigt. 
  
## <a name="see-also"></a>Siehe auch

- [MAPI-Tabellen](mapi-tables.md)

