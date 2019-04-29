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
  
Generiert einen Lese-oder nicht gelesenen Bericht für eine Nachricht.
  
```cpp
HRESULT ReadReceipt(
ULONG ulFlags,
LPMESSAGE lpReadMessage,
LPMESSAGE FAR * lppEmptyMessage
);
```

## <a name="parameters"></a>Parameter

 _ulFlags_
  
> in Eine Bitmaske von Flags, die die Generierung des Lese-oder nonread-Berichts steuert. Das folgende Flag kann festgelegt werden:
    
MAPI_NON_READ 
  
> Ein ungelesener Bericht wird generiert. Wenn MAPI_NON_READ nicht festgelegt ist, wird ein Lesebericht generiert.
    
 _lpReadMessage_
  
> in Ein Zeiger auf die Nachricht, über die der Bericht generiert werden soll.
    
 _lppEmptyMessage_
  
> [in, out] Bei der Eingabe zeigt _lppEmptyMessage_ auf einen Zeiger auf eine leere Nachricht. Bei der Ausgabe zeigt _lppEmptyMessage_ auf einen Zeiger auf die Bericht Meldung. 
    
## <a name="return-value"></a>Rückgabewert

S_OK 
  
> Der Bericht wurde erfolgreich generiert.
    
## <a name="remarks"></a>Bemerkungen

Die **IMAPISupport:: ReadReceipt** -Methode wird nur für Support Objekte des Nachrichtenspeicher Anbieters implementiert. Nachrichtenspeicher Anbieter rufen **ReadReceipt** auf, um MAPI anzuweisen, einen Lese-oder nicht gelesenen Bericht für die Nachricht zu generieren, auf die durch den _lpReadMessage_ -Parameter verwiesen wird. 
  
## <a name="notes-to-callers"></a>Hinweise für Aufrufer

Rufen Sie **ReadReceipt** auf, wenn die **PR_READ_RECEIPT_REQUESTED** ([pidtagreadreceiptrequested (](pidtagreadreceiptrequested-canonical-property.md))-Eigenschaft festgelegt ist und eine der folgenden Bedingungen zutrifft:
  
- Die Nachricht wurde gelesen.
    
- Die Nachricht wurde verschoben.
    
- Die Nachricht wurde kopiert.
    
- Die [IMessage:: SetReadFlag](imessage-setreadflag.md) -Methode der Nachricht wurde aufgerufen. 
    
Rufen Sie **ReadReceipt** nicht auf, wenn eine Nachricht gelöscht wird. 
  
Ein Lese-oder ungelesener Bericht sollte nur einmal für eine Nachricht gesendet werden. Verfolgen Sie den Lesestatus einer Nachricht, und senden Sie nicht mehrere Berichte für eine einzelne Nachricht.
  
Wenn der _lppEmptyMessage_ -Parameter auf eine gültige Bericht Meldung zeigt, wenn MAPI von **ReadReceipt**zurückgegeben wird, rufen Sie die [IMessage:: SubmitMessage](imessage-submitmessage.md) -Methode auf, um die Nachricht zu senden, und lassen Sie den Zeiger dann durch Aufrufen des **IUnknown: s: Release **-Methode. 
  
Wenn **ReadReceipt** fehlschlägt, sollte die Nachricht ohne übermittelt werden. Wenn Sie den Lesestatus der Nachricht speichern, können Sie versuchen, den Lese-oder nonread-Bericht zu einem späteren Zeitpunkt zu generieren. 
  
Sie können Lese-und nonread-Berichte, die von Speichern in Ihren Ordnern generiert wurden, entweder ausblenden oder anzeigen. Durch das Speichern von Lese-und nonread-Berichten in ausgeblendeten Ordnern können Sie eine engere Sicherheit implementieren.
  
## <a name="see-also"></a>Siehe auch



[IMAPIFolder::DeleteMessages](imapifolder-deletemessages.md)
  
[IMessage::SubmitMessage](imessage-submitmessage.md)
  
[Kanonische Pidtagreadreceiptrequested (-Eigenschaft](pidtagreadreceiptrequested-canonical-property.md)
  
[IMAPISupport: IUnknown](imapisupportiunknown.md)

