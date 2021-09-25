---
title: IMAPISupportReadReceipt
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
ms.localizationpriority: medium
api_name:
- IMAPISupport.ReadReceipt
api_type:
- COM
ms.assetid: ef31b61a-93b6-4ae8-bc71-f5ef5caf43f4
description: 'Letzte Änderung: Samstag, 23. Juli 2011'
ms.openlocfilehash: bd008c7233b191c3e187f6cc44767a9b136a2df8
ms.sourcegitcommit: a1d9041c20256616c9c183f7d1049142a7ac6991
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 09/24/2021
ms.locfileid: "59625406"
---
# <a name="imapisupportreadreceipt"></a>IMAPISupport::ReadReceipt

  
  
**Gilt für**: Outlook 2013 | Outlook 2016 
  
Generiert einen gelesenen oder nicht gelesenen Bericht für eine Nachricht.
  
```cpp
HRESULT ReadReceipt(
ULONG ulFlags,
LPMESSAGE lpReadMessage,
LPMESSAGE FAR * lppEmptyMessage
);
```

## <a name="parameters"></a>Parameter

 _ulFlags_
  
> [in] Eine Bitmaske mit Flags, die steuert, wie der gelesene oder nicht gelesene Bericht generiert wird. Das folgende Kennzeichen kann festgelegt werden:
    
MAPI_NON_READ 
  
> Ein nicht gelesener Bericht wird generiert. Wenn MAPI_NON_READ nicht festgelegt ist, wird ein Lesebericht generiert.
    
 _lpReadMessage_
  
> [in] Ein Zeiger auf die Nachricht, über die der Bericht generiert werden soll.
    
 _lppEmptyMessage_
  
> [in, out] Bei der Eingabe zeigt  _lppEmptyMessage_ auf einen Zeiger auf eine leere Nachricht. Bei der Ausgabe zeigt  _lppEmptyMessage_ auf einen Zeiger auf die Berichtsnachricht. 
    
## <a name="return-value"></a>Rückgabewert

S_OK 
  
> Der Bericht wurde erfolgreich generiert.
    
## <a name="remarks"></a>Bemerkungen

Die **IMAPISupport::ReadReceipt-Methode** wird nur für Supportobjekte des Nachrichtenspeicheranbieters implementiert. Nachrichtenspeicheranbieter rufen **ReadReceipt** auf, um die MAPI anzuweisen, einen lese- oder nicht gelesenen Bericht für die Nachricht zu generieren, auf die der  _lpReadMessage-Parameter_ verweist. 
  
## <a name="notes-to-callers"></a>Hinweise für Aufrufer

Rufen Sie **ReadReceipt** auf, wenn die **Eigenschaft PR_READ_RECEIPT_REQUESTED** ([PidTagReadReceiptRequested](pidtagreadreceiptrequested-canonical-property.md)) festgelegt ist und eine der folgenden Bedingungen erfüllt ist:
  
- Die Nachricht wurde gelesen.
    
- Die Nachricht wurde verschoben.
    
- Die Nachricht wurde kopiert.
    
- Die [IMessage::SetReadFlag-Methode](imessage-setreadflag.md) der Nachricht wurde aufgerufen. 
    
Rufen Sie **"ReadReceipt"** nicht auf, wenn eine Nachricht gelöscht wird. 
  
Ein gelesener oder nicht gelesener Bericht sollte nur einmal für eine Nachricht gesendet werden. Verfolgen Sie den Lesestatus einer Nachricht, und senden Sie nicht mehrere Berichte für eine einzelne Nachricht.
  
Wenn der  _Parameter lppEmptyMessage_ auf eine gültige Berichtsnachricht zeigt, wenn MAPI von **ReadReceipt** zurückgegeben wird, rufen Sie die [IMessage::SubmitMessage-Methode](imessage-submitmessage.md) auf, um die Nachricht zu senden, und geben Sie dann den Zeiger frei, indem Sie seine **IUnknown:s:Release-Methode** aufrufen. 
  
Wenn **ReadReceipt** fehlschlägt, sollte die Nachricht ohne Übermittlung freigegeben werden. Wenn Sie den Lesestatus der Nachricht speichern, können Sie zu einem späteren Zeitpunkt versuchen, den gelesenen oder nicht gelesenen Bericht zu generieren. 
  
Sie können lese- und nicht gelesene Berichte, die von Speichern in Ihren Ordnern generiert werden, ausblenden oder anzeigen. Wenn Sie Lese- und nicht gelesene Berichte in ausgeblendeten Ordnern speichern, können Sie eine strengere Sicherheit implementieren.
  
## <a name="see-also"></a>Siehe auch



[IMAPIFolder::DeleteMessages](imapifolder-deletemessages.md)
  
[IMessage::SubmitMessage](imessage-submitmessage.md)
  
[PidTagReadReceiptRequested (kanonische Eigenschaft)](pidtagreadreceiptrequested-canonical-property.md)
  
[IMAPISupport: IUnknown](imapisupportiunknown.md)

