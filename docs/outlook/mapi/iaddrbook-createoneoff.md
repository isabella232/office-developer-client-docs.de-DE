---
title: IAddrBookCreateOneOff
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- IAddrBook.CreateOneOff
api_type:
- COM
ms.assetid: bcacfbdf-edff-4810-a985-e6d2c9271901
description: 'Letzte Änderung: Montag, 9. März 2015'
ms.openlocfilehash: 980ac82c6f7fcb5771a6013b3fb033b0bdfd05e0
ms.sourcegitcommit: 8657170d071f9bcf680aba50b9c07f2a4fb82283
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 04/28/2019
ms.locfileid: "33427381"
---
# <a name="iaddrbookcreateoneoff"></a>IAddrBook::CreateOneOff

  
  
**Gilt für**: Outlook 2013 | Outlook 2016 
  
Erstellt eine Eintrags-ID für eine einmalige Adresse.
  
```cpp
HRESULT CreateOneOff(
  LPSTR lpszName,
  LPSTR lpszAdrType,
  LPSTR lpszAddress,
  ULONG ulFlags,
  ULONG FAR * lpcbEntryID,
  LPENTRYID FAR * lppEntryID
);
```

## <a name="parameters"></a>Parameter

 _lpszName_
  
> in Ein Zeiger auf den Wert der **PR_DISPLAY_NAME** ([PidTagDisplayName](pidtagdisplayname-canonical-property.md))-Eigenschaft des Empfängers. Der _lpszName_ -Parameter kann NULL sein. 
    
 _lpszAdrType_
  
> in Ein Zeiger auf den Adresstyp des Empfängers, wie FAX oder SMTP. Der _lpszAdrType_ -Parameter darf nicht NULL sein. 
    
 _lpszAddress_
  
> in Ein Zeiger auf die Adresse des Empfängers. Der _lpszAddress_ -Parameter darf nicht NULL sein. 
    
 _ulFlags_
  
> in Eine Bitmaske von Flags, die sich auf den einmaligen Empfänger auswirkt. Die folgenden Flags können festgelegt werden:
    
MAPI_SEND_NO_RICH_INFO 
  
> Der Empfänger kann formatierten Nachrichteninhalt nicht verarbeiten. Wenn MAPI_SEND_NO_RICH_INFO festgelegt ist, legt MAPI die **PR_SEND_RICH_INFO** ([pidtagsendrichinfo (](pidtagsendrichinfo-canonical-property.md))-Eigenschaft des Empfängers auf false fest. Wenn MAPI_SEND_NO_RICH_INFO nicht festgelegt ist, legt MAPI diese Eigenschaft auf TRUE fest, es sei denn, die Messaging Adresse des Empfängers, auf die durch _lpszAddress_ verwiesen wird, wird als Internet Adresse interpretiert. In diesem Fall wird **PR_SEND_RICH_INFO** auf false festgelegt. 
    
MAPI_UNICODE 
  
> Der Anzeigename, der Adresstyp und die Adresse sind im Unicode-Format. Wenn das MAPI_UNICODE-Flag nicht festgelegt ist, sind diese Zeichenfolgen im ANSI-Format.
    
 _lpcbEntryID_
  
> Out Ein Zeiger auf die Bytezahl in der Eintrags-ID, auf die durch den _lppEntryID_ -Parameter verwiesen wird. 
    
 _lppEntryID_
  
> Out Ein Zeiger auf einen Zeiger auf die Eintrags-ID für den einmaligen Empfänger.
    
## <a name="return-value"></a>Rückgabewert

S_OK 
  
> Der einmalige Eintragsbezeichner wurde erfolgreich erstellt.
    
## <a name="remarks"></a>Bemerkungen

Clients rufen die **CreateOneOff** -Methode auf, um eine Eintrags-ID für einen einmaligen Empfänger zu erstellen: einen Empfänger, der keinem der Container eines der derzeit geladenen Adressbuchanbieter angehört. Einmal Empfänger können jede Art von Adresse haben, die von einem der aktiven Adressbuchanbieter für die Sitzung unterstützt wird. 
  
Einmal Empfänger werden in der Regel mit einer Vorlage für ihren jeweiligen Adresstyp erstellt. Der Adressbuchanbieter, der den Adresstyp unterstützt, liefert die Vorlage. Ein Benutzer einer Clientanwendung gibt die relevanten Informationen in die Vorlage ein.
  
MAPI unterstützt Unicode-Zeichenfolgen für den Anzeigenamen, den Adresstyp und die Adressparameter von **CreateOneOff**.
  
Das MAPI_SEND_NO_RICH_INFO-Flag steuert, ob formatierter Text im Rich-Text-Format (RTF) zusammen mit jeder Nachricht gesendet wird. Das Transport Neutral Encapsulation Format (TNEF) – ein Format, das für die Übertragung von formatiertem Text verwendet wird – wird von den meisten Transport Anbietern gesendet, unabhängig davon, wie der Empfänger seine **PR_SEND_RICH_INFO** -Eigenschaft festlegt. Dies ist kein Problem für Messaging-Clients, die mit zwischenmenschlichen Nachrichten arbeiten. Da TNEF jedoch normalerweise zum Senden benutzerdefinierter Eigenschaften für benutzerdefinierte Nachrichtenklassen verwendet wird, kann dies ein Problem für formularbasierte Clients oder Clients sein, die benutzerdefinierte MAPI-Eigenschaften erfordern. Weitere Informationen finden Sie unter [Senden von Nachrichten mit TNEF](sending-messages-with-tnef.md).
  
## <a name="mfcmapi-reference"></a>MFCMAPI-Referenz

Einen MFCMAP-Beispielcode finden Sie in der folgenden Tabelle.
  
|**Datei**|**Funktion**|**Comment**|
|:-----|:-----|:-----|
|Mapiabfunctions. cpp  <br/> |AddOneOffAddress  <br/> |MFCMAPI verwendet die **CreateOneOff** -Methode, um eine EINTRAGS-ID für eine Adresse zu erstellen, die in keinem Adressbuch gefunden wird.  <br/> |
   
## <a name="see-also"></a>Siehe auch



[IMAPISupport::CreateOneOff](imapisupport-createoneoff.md)
  
[IAddrBook : IMAPIProp](iaddrbookimapiprop.md)


[MFCMAPI (engl.) als ein Codebeispiel](mfcmapi-as-a-code-sample.md)

