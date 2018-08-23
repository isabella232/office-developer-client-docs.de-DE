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
ms.openlocfilehash: e785d42639d51dab154a0bde239f858a92ddd143
ms.sourcegitcommit: 0cf39e5382b8c6f236c8a63c6036849ed3527ded
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/23/2018
ms.locfileid: "22588622"
---
# <a name="imapisupportreadreceipt"></a>IMAPISupport::ReadReceipt

  
  
**Betrifft**: Outlook 2013 | Outlook 2016 
  
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
    
## <a name="remarks"></a>HinwBemerkungeneise

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
  
[PidTagReadReceiptRequested (kanonische Eigenschaft)](pidtagreadreceiptrequested-canonical-property.md)
  
[IMAPISupport: IUnknown](imapisupportiunknown.md)

