---
title: IAddrBookCreateOneOff
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
ms.localizationpriority: medium
api_name:
- IAddrBook.CreateOneOff
api_type:
- COM
ms.assetid: bcacfbdf-edff-4810-a985-e6d2c9271901
description: 'Letzte Änderung: Montag, 9. März 2015'
ms.openlocfilehash: e5eec965f4a70a5fdec1e9e97cfadc7d26294b78
ms.sourcegitcommit: a1d9041c20256616c9c183f7d1049142a7ac6991
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 09/24/2021
ms.locfileid: "59596442"
---
# <a name="iaddrbookcreateoneoff"></a>IAddrBook::CreateOneOff

  
  
**Gilt für**: Outlook 2013 | Outlook 2016 
  
Erstellt einen Eintragsbezeichner für eine einmalige Adresse.
  
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
  
> [in] Ein Zeiger auf den Wert der **PR_DISPLAY_NAME** ([PidTagDisplayName](pidtagdisplayname-canonical-property.md)) -Eigenschaft des Empfängers. Der  _lpszName-Parameter_ kann NULL sein. 
    
 _lpszAdrType_
  
> [in] Ein Zeiger auf den Adresstyp des Empfängers, z. B. FAX oder SMTP. Der  _LpszAdrType-Parameter_ darf nicht NULL sein. 
    
 _lpszAddress_
  
> [in] Ein Zeiger auf die Adresse des Empfängers. Der  _Parameter lpszAddress_ darf nicht NULL sein. 
    
 _ulFlags_
  
> [in] Eine Bitmaske von Flags, die sich auf den einmaligen Empfänger auswirkt. Die folgenden Flags können festgelegt werden:
    
MAPI_SEND_NO_RICH_INFO 
  
> Der Empfänger kann formatierte Nachrichteninhalte nicht verarbeiten. Wenn MAPI_SEND_NO_RICH_INFO festgelegt ist, legt MAPI die **eigenschaft PR_SEND_RICH_INFO** ([PidTagSendRichInfo](pidtagsendrichinfo-canonical-property.md)) des Empfängers auf FALSE fest. Wenn MAPI_SEND_NO_RICH_INFO nicht festgelegt ist, legt MAPI diese Eigenschaft auf TRUE fest, es sei denn, die Messagingadresse des Empfängers, auf die von  _lpszAddress_ verwiesen wird, wird als Internetadresse interpretiert. In diesem Fall legt MAPI **PR_SEND_RICH_INFO** auf FALSE fest. 
    
MAPI_UNICODE 
  
> Der Anzeigename, der Adresstyp und die Adresse haben das Unicode-Format. Wenn das flag MAPI_UNICODE nicht festgelegt ist, haben diese Zeichenfolgen das ANSI-Format.
    
 _lpcbEntryID_
  
> [out] Ein Zeiger auf die Byteanzahl im Eintragsbezeichner, auf den der  _Parameter "lppEntryID"_ verweist. 
    
 _lppEntryID_
  
> [out] Ein Zeiger auf einen Zeiger auf den Eintragsbezeichner für den einmaligen Empfänger.
    
## <a name="return-value"></a>Rückgabewert

S_OK 
  
> Der einmalige Eintragsbezeichner wurde erfolgreich erstellt.
    
## <a name="remarks"></a>HinwBemerkungeneise

Clients rufen die **CreateOneOff-Methode** auf, um einen Eintragsbezeichner für einen einmaligen Empfänger zu erstellen – einen Empfänger, der keinem der Container von einem der aktuell geladenen Adressbuchanbieter angehört. Einmalige Empfänger können jede Art von Adresse haben, die von einem der aktiven Adressbuchanbieter für die Sitzung unterstützt wird. 
  
Einmalige Empfänger werden in der Regel mit einer Vorlage für ihren bestimmten Adresstyp erstellt. Der Adressbuchanbieter, der den Adresstyp unterstützt, stellt die Vorlage bereit. Ein Benutzer einer Clientanwendung gibt die relevanten Informationen in die Vorlage ein.
  
MAPI unterstützt Unicode-Zeichenzeichenfolgen für den Anzeigenamen, den Adresstyp und die Adressparameter von **CreateOneOff.**
  
Die MAPI_SEND_NO_RICH_INFO-Kennzeichnung steuert, ob formatierter Text im RtF-Format (Rich Text Format) zusammen mit jeder Nachricht gesendet wird. Das Transport Neutral Encapsulation Format (TNEF) – ein Format, das für die Übertragung von formatiertem Text verwendet wird – wird von den meisten Transportanbietern gesendet, unabhängig davon, wie der Empfänger seine **PR_SEND_RICH_INFO-Eigenschaft** festlegt. Dies ist kein Problem für Messaging-Clients, die mit zwischenmenschlichen Nachrichten arbeiten. Da TNEF jedoch in der Regel zum Senden benutzerdefinierter Eigenschaften für benutzerdefinierte Nachrichtenklassen verwendet wird, kann die Nichtunterstützung für formularbasierte Clients oder Clients, die benutzerdefinierte MAPI-Eigenschaften erfordern, ein Problem darstellen. Weitere Informationen finden Sie unter [Senden von Nachrichten mit TNEF.](sending-messages-with-tnef.md)
  
## <a name="mfcmapi-reference"></a>MFCMAPI-Referenz

Einen MFCMAP-Beispielcode finden Sie in der folgenden Tabelle.
  
|**Datei**|**Funktion**|**Comment**|
|:-----|:-----|:-----|
|Mapiabfunctions.cpp  <br/> |AddOneOffAddress  <br/> |MFCMAPI verwendet die **CreateOneOff-Methode,** um eine Eintrags-ID für eine Adresse zu erstellen, die in keinem Adressbuch gefunden wird.  <br/> |
   
## <a name="see-also"></a>Siehe auch



[IMAPISupport::CreateOneOff](imapisupport-createoneoff.md)
  
[IAddrBook : IMAPIProp](iaddrbookimapiprop.md)


[MFCMAPI (engl.) als ein Codebeispiel](mfcmapi-as-a-code-sample.md)

