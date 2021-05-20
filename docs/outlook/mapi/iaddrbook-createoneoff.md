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
  
Erstellt einen Eintragsbezeichner für eine eindeutige Adresse.
  
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
  
> [in] Ein Zeiger auf den Wert der PR_DISPLAY_NAME **(** [PidTagDisplayName](pidtagdisplayname-canonical-property.md)) Eigenschaft des Empfängers. Der  _lpszName-Parameter_ kann NULL sein. 
    
 _lpszAdrType_
  
> [in] Ein Zeiger auf den Adresstyp des Empfängers, z. B. FAX oder SMTP. Der  _lpszAdrType-Parameter_ darf nicht NULL sein. 
    
 _lpszAddress_
  
> [in] Ein Zeiger auf die Adresse des Empfängers. Der  _lpszAddress-Parameter_ darf nicht NULL sein. 
    
 _ulFlags_
  
> [in] Eine Bitmaske mit Flags, die sich auf den einmalen Empfänger auswirkt. Die folgenden Kennzeichen können festgelegt werden:
    
MAPI_SEND_NO_RICH_INFO 
  
> Der Empfänger kann formatierte Nachrichteninhalte nicht verarbeiten. Wenn MAPI_SEND_NO_RICH_INFO festgelegt ist, legt MAPI die **Eigenschaft PR_SEND_RICH_INFO** ([PidTagSendRichInfo](pidtagsendrichinfo-canonical-property.md)) des Empfängers auf FALSE fest. Wenn MAPI_SEND_NO_RICH_INFO nicht festgelegt ist, legt MAPI diese Eigenschaft auf TRUE fest, es sei denn, die von  _lpszAddress_ angezeigte Messagingadresse des Empfängers wird als Internetadresse interpretiert. In diesem Fall legt MAPI **PR_SEND_RICH_INFO** FALSE fest. 
    
MAPI_UNICODE 
  
> Anzeigename, Adresstyp und Adresse befinden sich im Unicode-Format. Wenn das MAPI_UNICODE nicht festgelegt ist, sind diese Zeichenfolgen im ANSI-Format.
    
 _lpcbEntryID_
  
> [out] Ein Zeiger auf die Byteanzahl in der Eintrags-ID, auf die der  _lppEntryID-Parameter_ verweist. 
    
 _lppEntryID_
  
> [out] Ein Zeiger auf einen Zeiger auf die Eintrags-ID für den einmal verwendeten Empfänger.
    
## <a name="return-value"></a>Rückgabewert

S_OK 
  
> Der eindeutige Eintragsbezeichner wurde erfolgreich erstellt.
    
## <a name="remarks"></a>Hinweise

Clients rufen die **CreateOneOff-Methode** auf, um eine Eintrags-ID für einen einzigen Empfänger zu erstellen – einen Empfänger, der keinem der Container von einem der derzeit geladenen Adressbuchanbieter angehört. Einmalempfänger können über eine beliebige Art von Adresse verfügen, die von einem der aktiven Adressbuchanbieter für die Sitzung unterstützt wird. 
  
Einmalempfänger werden in der Regel mit einer Vorlage für ihren bestimmten Adresstyp erstellt. Der Adressbuchanbieter, der den Adresstyp unterstützt, liefert die Vorlage. Ein Benutzer einer Clientanwendung gibt die relevanten Informationen in die Vorlage ein.
  
MAPI unterstützt Unicode-Zeichenzeichenfolgen für den Anzeigenamen, den Adresstyp und die Adressparameter von **CreateOneOff**.
  
Das MAPI_SEND_NO_RICH_INFO steuert, ob formatierter Text im Rich Text Format (RTF) zusammen mit jeder Nachricht gesendet wird. Das Transport Neutral Encapsulation Format (TNEF) – ein Format, das für die Übertragung von formatiertem Text verwendet wird – wird von den meisten Transportanbietern gesendet, unabhängig davon, wie der Empfänger seine **PR_SEND_RICH_INFO** legt. Dies ist kein Problem für Messagingclients, die mit zwischenmenschlichen Nachrichten arbeiten. Da TNEF jedoch in der Regel zum Senden benutzerdefinierter Eigenschaften für benutzerdefinierte Nachrichtenklassen verwendet wird, kann dies bei formularbasierten Clients oder Clients, die benutzerdefinierte MAPI-Eigenschaften erfordern, ein Problem sein, wenn sie nicht unterstützt werden. Weitere Informationen finden Sie unter [Senden von Nachrichten mit TNEF](sending-messages-with-tnef.md).
  
## <a name="mfcmapi-reference"></a>MFCMAPI-Referenz

Einen MFCMAP-Beispielcode finden Sie in der folgenden Tabelle.
  
|**Datei**|**Funktion**|**Comment**|
|:-----|:-----|:-----|
|Mapiabfunctions.cpp  <br/> |AddOneOffAddress  <br/> |MFCMAPI verwendet die **CreateOneOff-Methode,** um eine Eintrags-ID für eine Adresse zu erstellen, die in keinem Adressbuch gefunden wird.  <br/> |
   
## <a name="see-also"></a>Siehe auch



[IMAPISupport::CreateOneOff](imapisupport-createoneoff.md)
  
[IAddrBook : IMAPIProp](iaddrbookimapiprop.md)


[MFCMAPI (engl.) als ein Codebeispiel](mfcmapi-as-a-code-sample.md)

