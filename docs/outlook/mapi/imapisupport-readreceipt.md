---
title: IMAPISupportReadReceipt
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- IMAPISupport.ReadReceipt
api_type:
- COM
ms.assetid: ef31b61a-93b6-4ae8-bc71-f5ef5caf43f4
description: 'Letzte Änderung: Samstag, 23. Juli 2011'
ms.openlocfilehash: 1915004847fdfd27c97656223866aaab9d3e59c9
ms.sourcegitcommit: 8657170d071f9bcf680aba50b9c07f2a4fb82283
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 04/28/2019
ms.locfileid: "33425323"
---
# <a name="imapisupportreadreceipt"></a>IMAPISupport::ReadReceipt

  
  
**Gilt für**: Outlook 2013 | Outlook 2016 
  
Generiert einen lese- oder nicht gelesenen Bericht für eine Nachricht.
  
```cpp
HRESULT ReadReceipt(
ULONG ulFlags,
LPMESSAGE lpReadMessage,
LPMESSAGE FAR * lppEmptyMessage
);
```

## <a name="parameters"></a>Parameter

 _ulFlags_
  
> [in] Eine Bitmaske mit Flags, die steuert, wie der Lese- oder Ungelesenbericht generiert wird. Das folgende Flag kann festgelegt werden:
    
MAPI_NON_READ 
  
> Ein nicht gelesener Bericht wird generiert. Wenn MAPI_NON_READ nicht festgelegt ist, wird ein Lesebericht generiert.
    
 _lpReadMessage_
  
> [in] Ein Zeiger auf die Nachricht, über die der Bericht generiert werden soll.
    
 _lppEmptyMessage_
  
> [in, out] Bei der Eingabe  _zeigt lppEmptyMessage_ auf einen Zeiger auf eine leere Nachricht. Bei der Ausgabe  _zeigt lppEmptyMessage_ auf einen Zeiger auf die Berichtsnachricht. 
    
## <a name="return-value"></a>Rückgabewert

S_OK 
  
> Der Bericht wurde erfolgreich generiert.
    
## <a name="remarks"></a>Hinweise

Die **IMAPISupport::ReadReceipt-Methode** wird nur für Unterstützungsobjekte des Nachrichtenspeicheranbieters implementiert. Nachrichtenspeicheranbieter rufen **ReadReceipt** auf, um MAPI anweisen, einen Lese- oder Ungelesenbericht für die Nachricht zu generieren, auf die der  _lpReadMessage-Parameter_ verweist. 
  
## <a name="notes-to-callers"></a>Hinweise für Aufrufer

Rufen **Sie ReadReceipt** **auf,** wenn die PR_READ_RECEIPT_REQUESTED ([PidTagReadReceiptRequested](pidtagreadreceiptrequested-canonical-property.md)) -Eigenschaft festgelegt ist und eine der folgenden Bedingungen true ist:
  
- Die Nachricht wurde gelesen.
    
- Die Nachricht wurde verschoben.
    
- Die Nachricht wurde kopiert.
    
- Die [IMessage::SetReadFlag-Methode](imessage-setreadflag.md) der Nachricht wurde aufgerufen. 
    
Rufen Sie **ReadReceipt nicht auf,** wenn eine Nachricht gelöscht wird. 
  
Ein gelesener oder nicht gelesener Bericht sollte nur einmal für eine Nachricht gesendet werden. Verfolgen Sie den Lesestatus einer Nachricht, und senden Sie nicht mehrere Berichte für eine einzelne Nachricht.
  
Wenn der  _lppEmptyMessage-Parameter_ auf eine gültige Berichtsnachricht verweist, wenn MAPI von **ReadReceipt** zurückgibt, rufen Sie die [IMessage::SubmitMessage-Methode](imessage-submitmessage.md) auf, um die Nachricht zu senden, und geben Sie dann den Zeiger frei, indem Sie die **IUnknown:s:Release-Methode** aufrufen. 
  
Wenn **ReadReceipt fehlschlägt,** sollte die Nachricht ohne Übermittelte freigegeben werden. Wenn Sie den Lesestatus der Nachricht speichern, können Sie zu einem späteren Zeitpunkt versuchen, den Lese- oder Ungelesenbericht zu generieren. 
  
Sie können lese- und nicht gelesene Berichte, die von Speichern in Ihren Ordnern generiert werden, ausblenden oder anzeigen. Durch das Speichern von Lese- und Ungelesenberichten in ausgeblendeten Ordnern können Sie eine strengere Sicherheit implementieren.
  
## <a name="see-also"></a>Siehe auch



[IMAPIFolder::DeleteMessages](imapifolder-deletemessages.md)
  
[IMessage::SubmitMessage](imessage-submitmessage.md)
  
[PidTagReadReceiptRequested (kanonische Eigenschaft)](pidtagreadreceiptrequested-canonical-property.md)
  
[IMAPISupport: IUnknown](imapisupportiunknown.md)

