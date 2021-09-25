---
title: IMAPITableCreateBookmark
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
ms.localizationpriority: medium
api_name:
- IMAPITable.CreateBookmark
api_type:
- COM
ms.assetid: 320af2ff-c2a5-43b1-b3a1-76cb5ffd6a4f
description: 'Letzte Änderung: Samstag, 23. Juli 2011'
ms.openlocfilehash: e3605dc630b6a7bcff46aa3a038d4a4ec7a1f114
ms.sourcegitcommit: a1d9041c20256616c9c183f7d1049142a7ac6991
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 09/24/2021
ms.locfileid: "59600967"
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
  
> [out] Zeiger auf den zurückgegebenen 32-Bit-Textmarkenwert. Diese Textmarke kann später in einem Aufruf der [IMAPITable::SeekRow-Methode](imapitable-seekrow.md) übergeben werden. 
    
## <a name="return-value"></a>Rückgabewert

S_OK 
  
> Der Aufruf erfolgreich ausgef�hrt und der erwartete Wert oder Werte zur�ckgegeben hat.
    
MAPI_E_UNABLE_TO_COMPLETE 
  
> Der angeforderte Vorgang konnte nicht abgeschlossen werden.
    
## <a name="remarks"></a>HinwBemerkungeneise

Die **IMAPITable::CreateBookmark-Methode** markiert eine Tabellenposition, indem ein Wert erstellt wird, der als Textmarke bezeichnet wird. Ein Lesezeichen kann verwendet werden, um an die von der Textmarke identifizierte Position zurückzukehren. Die Position der Textmarke ist dem Objekt in dieser Zeile in der Tabelle zugeordnet. 
  
Lesezeichen werden in Anlagentabellen nicht unterstützt, und Anlagentabellenimplementierungen von **CreateBookmark** geben MAPI_E_NO_SUPPORT zurück. 
  
## <a name="notes-to-implementers"></a>Hinweise für Implementierer

Aufgrund der Speicherkosten für die Verwaltung von Cursorpositionen mit Textmarken schränken Sie die Anzahl der Textmarken ein, die Sie erstellen können. Wenn Sie diese Nummer erreichen, geben Sie MAPI_E_UNABLE_TO_COMPLETE von allen nachfolgenden Aufrufen an **CreateBookmark** zurück.
  
Manchmal zeigt eine Textmarke auf eine Zeile, die sich nicht mehr in der Tabellenansicht befindet. Wenn ein Aufrufer eine solche Textmarke verwendet, verschieben Sie den Cursor zur nächsten sichtbaren Zeile, und beenden Sie dort. 
  
Wenn der Aufrufer versucht, eine Textmarke zu verwenden, die auf eine nicht lesbare Zeile verweist, da sie reduziert wurde, geben Sie MAPI_W_POSITION_CHANGED nach dem Verschieben der Textmarke zurück. Sie können die Textmarke entweder zu diesem Zeitpunkt oder beim Reduzieren in der **SetCollapseState-Methode** in die nächste sichtbare Zeile ändern. Wenn Sie das Lesezeichen zu dem Zeitpunkt verschieben, zu dem die Zeile reduziert ist, müssen Sie ein Bit in der Textmarke beibehalten, das genau angibt, wann die Textmarke verschoben wurde: seit der letzten Verwendung oder wenn sie seit der Erstellung nie verwendet wurde. 
  
## <a name="notes-to-callers"></a>Hinweise für Aufrufer

 **CreateBookmark** weist Speicher für die von ihm erstellte Textmarke zu. Geben Sie die Ressourcen für die Textmarke frei, indem Sie die [IMAPITable::FreeBookmark-Methode](imapitable-freebookmark.md) aufrufen. 
  
## <a name="see-also"></a>Siehe auch



[IMAPITable::FreeBookmark](imapitable-freebookmark.md)
  
[IMAPITable::SeekRow](imapitable-seekrow.md)
  
[IMAPITable : IUnknown](imapitableiunknown.md)

