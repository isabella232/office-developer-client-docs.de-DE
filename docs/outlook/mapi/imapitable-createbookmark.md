---
title: IMAPITableCreateBookmark
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- IMAPITable.CreateBookmark
api_type:
- COM
ms.assetid: 320af2ff-c2a5-43b1-b3a1-76cb5ffd6a4f
description: 'Letzte �nderung: Samstag, 23. Juli 2011'
ms.openlocfilehash: 34bd6de95f731c03466f19e0bc4fd6e2c9910900
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 06/11/2018
ms.locfileid: "19792445"
---
# <a name="imapitablecreatebookmark"></a>IMAPITable::CreateBookmark

  
  
**Betrifft**: Outlook 
  
Erstellt eine Textmarke an der aktuellen Position der Tabelle an.
  
```cpp
HRESULT CreateBookmark(
BOOKMARK FAR * lpbkPosition
);
```

## <a name="parameters"></a>Parameter

 _lpbkPosition_
  
> [out] Zeiger auf den zurückgegebenen Textmarke für 32-Bit-Wert. Dieses Lesezeichen kann später in einem Aufruf der [IMAPITable::SeekRow](imapitable-seekrow.md) -Methode übergeben werden. 
    
## <a name="return-value"></a>R�ckgabewert

S_OK 
  
> Der Aufruf erfolgreich ausgef�hrt und der erwartete Wert oder Werte zur�ckgegeben hat.
    
MAPI_E_UNABLE_TO_COMPLETE 
  
> Der angeforderte Vorgang konnte nicht abgeschlossen werden.
    
## <a name="remarks"></a>Bemerkungen

Die **IMAPITable::CreateBookmark** -Methode markiert die Position einer Tabelle, indem Sie einen Wert eine Textmarke namens erstellen. Eine Textmarke kann verwendet werden, um an der Position der Textmarke identifizierten zurückzugeben. Die mit einer Textmarke versehenen Position ist das Row-Objekts in der Tabelle-Objekt zugeordnet. 
  
Lesezeichen auf Anlagentabellen nicht unterstützt werden, und Anlage Tabelle Implementierungen von **CreateBookmark** MAPI_E_NO_SUPPORT zurückzugeben. 
  
## <a name="notes-to-implementers"></a>Hinweise für Implementierer

Aufgrund der Arbeitsspeicher Ausgaben Cursorpositionen mit Lesezeichen zu verwalten die Anzahl der Textmarken, die Sie erstellen können. Wenn diese Nummer erreicht ist, geben alle nachfolgenden Aufrufe **CreateBookmark**MAPI_E_UNABLE_TO_COMPLETE zurück.
  
In einigen Fällen zeigt ein Lesezeichen auf eine Zeile, die nicht mehr in der Tabellenansicht ist ein. Wenn ein Anrufer solche eine Textmarke verwendet wird, bewegen Sie den Cursor in die nächste Zeile sichtbar und noch mehr. 
  
Wenn der Aufrufer versucht, ein Lesezeichen zu verwenden, die auf ein sichtbares Zeile verweist, da es reduziert wurde, geben Sie nach dem Verschieben der Textmarke MAPI_W_POSITION_CHANGED zurück. Sie können die Textmarke in die nächste Zeile sichtbar zu diesem Zeitpunkt oder wenn tritt auf, in der **SetCollapseState** -Methode der reduzieren positionieren. Wenn Sie die Textmarke Zeitpunkt die Zeile reduziert ist verschieben, Sie müssen beibehalten etwas in die Textmarke, der angibt, wann genau die Textmarke verschoben wurde: seit der letzten verwenden, oder wenn es seit seiner Erstellung nie verwendet wurde. 
  
## <a name="notes-to-callers"></a>Hinweise für Aufrufer

 **CreateBookmark** weist Speicher für die Textmarke erstellt wird. Geben Sie die Ressourcen für das Lesezeichen durch Aufrufen der [IMAPITable::FreeBookmark](imapitable-freebookmark.md) -Methode. 
  
## <a name="see-also"></a>Siehe auch



[IMAPITable::FreeBookmark](imapitable-freebookmark.md)
  
[IMAPITable::SeekRow](imapitable-seekrow.md)
  
[IMAPITable : IUnknown](imapitableiunknown.md)

