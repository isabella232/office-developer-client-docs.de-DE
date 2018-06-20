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
description: 'Letzte �nderung: Samstag, 23. Juli 2011'
ms.openlocfilehash: 5e56fd8c053ff32bdeb7b243701c0330b378cdc0
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 06/11/2018
ms.locfileid: "19792423"
---
# <a name="imapisupportreadreceipt"></a>IMAPISupport::ReadReceipt

  
  
**Betrifft**: Outlook 
  
Generiert einen Lese- oder nonread Bericht für eine Nachricht.
  
```cpp
HRESULT ReadReceipt(
ULONG ulFlags,
LPMESSAGE lpReadMessage,
LPMESSAGE FAR * lppEmptyMessage
);
```

## <a name="parameters"></a>Parameter

 _ulFlags_
  
> [in] Eine Bitmaske aus Flags, die steuert, wie das Lesen oder den nonread Bericht generiert wird. Das folgende Flag kann festgelegt werden:
    
MAPI_NON_READ 
  
> Ein nonread Bericht generiert wird. Wenn MAPI_NON_READ nicht festgelegt ist, wird ein schreibgeschützte Bericht generiert.
    
 _lpReadMessage_
  
> [in] Ein Zeiger auf die Nachricht, die der Bericht generiert werden soll.
    
 _lppEmptyMessage_
  
> [in, out] Eingabe _LppEmptyMessage_ zeigt auf einen Zeiger auf eine leere Nachricht. Ausgabe _LppEmptyMessage_ zeigt auf einen Zeiger auf den Berichtnachricht. 
    
## <a name="return-value"></a>R�ckgabewert

S_OK 
  
> Der Bericht wurde erfolgreich generiert.
    
## <a name="remarks"></a>Hinweise

Die **IMAPISupport::ReadReceipt** -Methode ist nur für Nachricht Store Anbieter Unterstützungsobjekte implementiert. Nachricht-Anbieter anrufen **ReadReceipt** um anzuweisen, MAPI, um eine Lese- oder nonread Bericht für die Meldung über den Parameter _LpReadMessage_ generieren. 
  
## <a name="notes-to-callers"></a>Hinweise für Aufrufer

Rufen Sie **ReadReceipt** , wenn die Eigenschaft **PR_READ_RECEIPT_REQUESTED** ([PidTagReadReceiptRequested](pidtagreadreceiptrequested-canonical-property.md)) festgelegt ist und eine der folgenden Bedingungen zutrifft:
  
- Die Nachricht gelesen wurde.
    
- Die Nachricht wurde verschoben.
    
- Die Nachricht wurde kopiert.
    
- Die Nachricht [IMessage::SetReadFlag](imessage-setreadflag.md) -Methode wurde aufgerufen. 
    
Rufen Sie **ReadReceipt** nicht auf, wenn eine Nachricht gelöscht wird. 
  
Ein Lese- oder nonread Bericht soll nur einmal für eine Nachricht gesendet werden. Verfolgen einer Nachricht gelesen-Status und nicht senden Sie mehrere Berichte für eine Nachricht.
  
Wenn der Parameter _LppEmptyMessage_ mit einer gültigen Bericht Meldung zeigt MAPI aus **ReadReceipt**gibt, rufen Sie die [IMessage::SubmitMessage](imessage-submitmessage.md) -Methode zum Senden der Nachricht und klicken Sie dann den Zeiger durch Aufrufen der **IUnknown:s:Release-Version **Methode. 
  
Wenn **ReadReceipt** ein Fehler auftritt, sollten die Nachricht freigegeben werden, ohne gesendet wird. Wenn Sie die Nachricht gelesen-Status gespeichert werden sollen, können Sie versuchen, den Lese- oder nonread Bericht zu einem späteren Zeitpunkt zu generieren. 
  
Sie können entweder aus- oder Einblenden von Lese- und nonread Berichte vom Speicher in Ihrem Ordner generiert. Speichern von Lese- und nonread Berichten in verborgenen Ordnern können Sie eine engere Sicherheit zu implementieren.
  
## <a name="see-also"></a>Siehe auch



[IMAPIFolder::DeleteMessages](imapifolder-deletemessages.md)
  
[IMessage::SubmitMessage](imessage-submitmessage.md)
  
[Kanonische PidTagReadReceiptRequested-Eigenschaft](pidtagreadreceiptrequested-canonical-property.md)
  
[IMAPISupport: IUnknown](imapisupportiunknown.md)

