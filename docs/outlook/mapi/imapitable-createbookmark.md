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
description: 'Letzte Änderung: Samstag, 23. Juli 2011'
ms.openlocfilehash: c251dacce0d4e1743a74f1ba45e395b6e1c05064
ms.sourcegitcommit: 8657170d071f9bcf680aba50b9c07f2a4fb82283
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 04/28/2019
ms.locfileid: "33408824"
---
# <a name="imapitablecreatebookmark"></a>IMAPITable::CreateBookmark

  
  
**Gilt für**: Outlook 2013 | Outlook 2016 
  
Erstellt eine Textmarke an der aktuellen Position der Tabelle.
  
```cpp
HRESULT CreateBookmark(
BOOKMARK FAR * lpbkPosition
);
```

## <a name="parameters"></a>Parameter

 _lpbkPosition_
  
> [out] Zeiger auf den zurückgegebenen 32-Bit-Lesezeichenwert. Diese Textmarke kann später in einem Aufruf der [IMAPITable::SeekRow-Methode übergeben](imapitable-seekrow.md) werden. 
    
## <a name="return-value"></a>Rückgabewert

S_OK 
  
> Der Aufruf erfolgreich ausgef�hrt und der erwartete Wert oder Werte zur�ckgegeben hat.
    
MAPI_E_UNABLE_TO_COMPLETE 
  
> Der angeforderte Vorgang konnte nicht abgeschlossen werden.
    
## <a name="remarks"></a>Hinweise

Die **IMAPITable::CreateBookmark-Methode** markiert eine Tabellenposition, indem ein Wert erstellt wird, der als Lesezeichen bezeichnet wird. Eine Textmarke kann verwendet werden, um an die position zurückzukehren, die durch die Textmarke identifiziert wird. Die Position mit Textmarken ist dem Objekt in dieser Zeile in der Tabelle zugeordnet. 
  
Lesezeichen werden in Anlagentabellen nicht unterstützt, und Anlagentabellenimplementierungen von **CreateBookmark** geben MAPI_E_NO_SUPPORT. 
  
## <a name="notes-to-implementers"></a>Hinweise für Implementierer

Beschränken Sie aufgrund der Speicherkosten für die Verwaltung von Cursorpositionen mit Textmarken die Anzahl der Lesezeichen, die Sie erstellen können. Wenn Sie diese Nummer erreichen, geben MAPI_E_UNABLE_TO_COMPLETE von allen nachfolgenden Aufrufen an **CreateBookmark zurück.**
  
Manchmal verweist eine Textmarke auf eine Zeile, die sich nicht mehr in der Tabellenansicht befindet. Wenn ein Aufrufer ein solches Lesezeichen verwendet, verschieben Sie den Cursor zur nächsten sichtbaren Zeile, und halten Sie dort an. 
  
Wenn der Aufrufer versucht, eine Textmarke zu verwenden, die auf eine nicht lesbare Zeile verweisen soll, da sie reduziert wurde, geben Sie MAPI_W_POSITION_CHANGED nach dem Verschieben der Textmarke zurück. Sie können die Textmarke entweder zu diesem Zeitpunkt oder bei einem Kollaps in der **SetCollapseState-Methode** in der nächsten sichtbaren Zeile neu positionieren. Wenn Sie die Textmarke zu dem Zeitpunkt verschieben, zu dem die Zeile reduziert wird, müssen Sie ein Bit in der Textmarke beibehalten, das genau angibt, wann die Textmarke verschoben wurde: seit der letzten Verwendung oder wenn sie seit der Erstellung nie verwendet wurde. 
  
## <a name="notes-to-callers"></a>Hinweise für Aufrufer

 **CreateBookmark weist** dem erstellten Lesezeichen Arbeitsspeicher zu. Geben Sie die Ressourcen für die Textmarke frei, indem Sie die [IMAPITable::FreeBookmark-Methode](imapitable-freebookmark.md) aufrufen. 
  
## <a name="see-also"></a>Siehe auch



[IMAPITable::FreeBookmark](imapitable-freebookmark.md)
  
[IMAPITable::SeekRow](imapitable-seekrow.md)
  
[IMAPITable : IUnknown](imapitableiunknown.md)

