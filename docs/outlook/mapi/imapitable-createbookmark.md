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
  
> Out Zeiger auf den zurückgegebenen 32-Bit-Lesezeichenwert. Diese Textmarke kann später in einem Aufruf an die [IMAPITable:: SeekRow](imapitable-seekrow.md) -Methode übergeben werden. 
    
## <a name="return-value"></a>Rückgabewert

S_OK 
  
> Der Aufruf erfolgreich ausgef�hrt und der erwartete Wert oder Werte zur�ckgegeben hat.
    
MAPI_E_UNABLE_TO_COMPLETE 
  
> Der angeforderte Vorgang konnte nicht abgeschlossen werden.
    
## <a name="remarks"></a>Bemerkungen

Die **IMAPITable:: CreateBookMark** -Methode kennzeichnet eine Tabellenposition durch Erstellen eines Werts, der als Textmarke bezeichnet wird. Eine Textmarke kann verwendet werden, um zu der durch die Textmarke identifizierten Position zurückzukehren. Die Lesezeichenposition ist dem Objekt in dieser Zeile in der Tabelle zugeordnet. 
  
Lesezeichen werden für Anlagen Tabellen und für Anlagen Tabellen Implementierungen von **CreateBookMark** Return MAPI_E_NO_SUPPORT nicht unterstützt. 
  
## <a name="notes-to-implementers"></a>Hinweise für Implementierer

Aufgrund der Arbeitsspeicherkosten für die Verwaltung von Cursorpositionen mit Lesezeichen können Sie die Anzahl der zu erstellende Textmarken begrenzen. Wenn Sie diese Nummer erreicht haben, geben Sie MAPI_E_UNABLE_TO_COMPLETE von allen nachfolg **** enden Aufrufen von CreateBookMark zurück.
  
Manchmal verweist eine Textmarke auf eine Zeile, die sich nicht mehr in der Tabellenansicht befindet. Wenn ein Anrufer ein solches Lesezeichen verwendet, bewegen Sie den Cursor zur nächsten sichtbaren Zeile, und halten Sie dort an. 
  
Wenn der Aufrufer versucht, ein Lesezeichen zu verwenden, das auf eine nicht sichtbare Zeile zeigt, da es reduziert wurde, geben Sie MAPI_W_POSITION_CHANGED nach dem Bewegen der Textmarke zurück. Sie können die Textmarke entweder zu diesem Zeitpunkt oder in der **SetCollapseState** -Methode in die nächste sichtbare Zeile verschieben. Wenn Sie die Textmarke zu dem Zeitpunkt verschieben, zu dem die Zeile reduziert wird, müssen Sie ein Bit in der Textmarke aufbewahren, die genau angibt, wann das Lesezeichen verschoben wurde: seit der letzten Verwendung oder wenn es nie seit seiner Erstellung verwendet wurde. 
  
## <a name="notes-to-callers"></a>Hinweise für Aufrufer

 **CreateBookMark** reserviert Speicher für die erstellte Textmarke. Geben Sie die Ressourcen für das Lesezeichen frei, indem Sie die [IMAPITable:: FreeBookmark](imapitable-freebookmark.md) -Methode aufrufen. 
  
## <a name="see-also"></a>Siehe auch



[IMAPITable::FreeBookmark](imapitable-freebookmark.md)
  
[IMAPITable::SeekRow](imapitable-seekrow.md)
  
[IMAPITable : IUnknown](imapitableiunknown.md)

