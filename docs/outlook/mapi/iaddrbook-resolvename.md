---
title: IAddrBookResolveName
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
ms.localizationpriority: medium
api_name:
- IAddrBook.ResolveName
api_type:
- COM
ms.assetid: a7823c16-efda-45c2-b931-3e1fbc823b0b
description: 'Letzte Änderung: Montag, 9. März 2015'
ms.openlocfilehash: 9b371214b9f782fcf0afab0943c4a0654a5716d8
ms.sourcegitcommit: a1d9041c20256616c9c183f7d1049142a7ac6991
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 09/24/2021
ms.locfileid: "59610734"
---
# <a name="iaddrbookresolvename"></a>IAddrBook::ResolveName

  
  
**Gilt für**: Outlook 2013 | Outlook 2016 
  
Führt eine Namensauflösung durch und weist Empfängern in einer Empfängerliste Eintragsbezeichner zu.
  
```cpp
HRESULT ResolveName(
  ULONG_PTR ulUIParam,
  ULONG ulFlags,
  LPSTR lpszNewEntryTitle,
  LPADRLIST lpAdrList
);
```

## <a name="parameters"></a>Parameter

 _ulUIParam_
  
> [in] Ein handle to the parent window of a dialog box that is shown, if specified, to prompt the user to resolve ambiguity.
    
 _ulFlags_
  
> [in] Eine Bitmaske von Flags, die verschiedene Aspekte des Auflösungsprozesses steuern. Die folgenden Flags können festgelegt werden:
    
AB_UNICODEUI
  
> Gibt an, dass  _lpszNewEntryTitle_ eine UNICODE-Zeichenfolge ist. 
    
MAPI_CACHE_ONLY
  
> Verwenden Sie nur das Offlineadressbuch, um die Namensauflösung auszuführen. Beispielsweise können Sie dieses Flag verwenden, um einer Clientanwendung das Öffnen der globalen Adressliste (GAL) im Cache-Exchange-Modus und den Zugriff auf einen Eintrag in diesem Adressbuch aus dem Cache zu ermöglichen, ohne Datenverkehr zwischen dem Client und dem Server zu erstellen. Dieses Flag wird nur vom Exchange Adressbuchanbieter unterstützt.
    
MAPI_DIALOG 
  
> Zeigt ein Dialogfeld an, in dem der Benutzer zur Eingabe zusätzlicher Informationen zur Namensauflösung aufgefordert wird. Wenn dieses Kennzeichen nicht festgelegt ist, wird kein Dialogfeld angezeigt. 
    
MAPI_UNICODE 
  
> Gibt an, dass die in der Adressliste zurückgegebenen Eigenschaften vom Typ PT_UNICODE anstelle von PT_STRING8 sein sollten. 
    
 _lpszNewEntryTitle_
  
> [in] Ein Zeiger auf Text für den Titel des Steuerelements im Dialogfeld, der den Benutzer zur Eingabe eines Empfängers auffordert. Der Titel variiert je nach Empfängertyp. Der  _LpszNewEntryTitle-Parameter_ kann NULL sein. 
    
 _lpAdrList_
  
> [In-Out] Ein Zeiger auf eine [ADRLIST-Struktur,](adrlist.md) die die Liste der empfängernamen enthält, die aufgelöst werden sollen. Diese **ADRLIST-Struktur** kann mit der [IAddrBook::Address-Methode](iaddrbook-address.md) erstellt werden. 
    
## <a name="return-value"></a>Rückgabewert

S_OK 
  
> Der Vorgang zur Namensauflösung war erfolgreich.
    
MAPI_E_AMBIGUOUS_RECIP 
  
> Mindestens ein Empfänger im  _lpAdrList-Parameter_ stimmte mit mehreren Einträgen im Adressbuch überein. In der Regel wird dieser Wert zurückgegeben, wenn das MAPI_DIALOG-Kennzeichen festgelegt ist, wodurch die Anzeige eines Dialogfelds verhindert wird. 
    
MAPI_E_NOT_FOUND 
  
> Mindestens ein Empfänger im  _lpAdrList-Parameter_ kann nicht aufgelöst werden. In der Regel wird dieser Wert zurückgegeben, wenn das MAPI_DIALOG-Kennzeichen festgelegt ist, wodurch die Anzeige eines Dialogfelds verhindert wird. 
    
## <a name="remarks"></a>HinwBemerkungeneise

Clients und Dienstanbieter rufen die **ResolveName-Methode** auf, um den Namensauflösungsprozess zu initiieren. Ein nicht aufgelöster Eintrag ist ein Eintrag, der noch keinen Eintragsbezeichner oder **keine PR_ENTRYID** ([PidTagEntryId](pidtagentryid-canonical-property.md)) -Eigenschaft hat.
  
 **ResolveName** durchläuft den folgenden Prozess für jeden nicht aufgelösten Eintrag in der Adressliste, der im  _lpAdrList-Parameter_ übergeben wird. 
  
1. Wenn der Adresstyp des Empfängers dem Format einer SMTP-Adresse ( _Anzeigename_ @  _domain.top Domäne auf Ebene)_ entspricht, weist **ResolveName** ihm einen einmaligen Eintragsbezeichner zu. 
    
2. Für jeden Container in der **eigenschaft PR_AB_SEARCH_PATH** ([PidTagAbSearchPath](pidtagabsearchpath-canonical-property.md)) ruft **ResolveName** die [IABContainer::ResolveNames-Methode](iabcontainer-resolvenames.md) auf. **ResolveNames** versucht, den Anzeigenamen jedes nicht aufgelösten Empfängers mit einem Anzeigenamen zuzuordnen, der zu einem seiner Einträge gehört. 
    
3. Wenn ein Container **ResolveNames** nicht unterstützt, schränkt **ResolveName** das Inhaltsverzeichnis des Containers mithilfe einer **PR_ANR** ([PidTagAnr](pidtaganr-canonical-property.md)) -Eigenschaftseinschränkung ein. Diese Einschränkung bewirkt, dass der Container eine "best guess"-Suchart durchführt, um einen übereinstimmenden Empfänger zu finden. Alle Container müssen die **PR_ANR** Eigenschaftseinschränkung unterstützen. 
    
4. Wenn ein Container einen Empfänger zurückgibt, der mit mehreren Namen übereinstimmt, zeigt **ResolveName** ein Dialogfeld an, wenn das flag MAPI_DIALOG festgelegt ist, in dem der Benutzer den richtigen Namen auswählen kann. 
    
5. Wenn alle Container in der **PR_AB_SEARCH_PATH-Eigenschaft** aufgerufen wurden und keine Übereinstimmung gefunden wurde, bleibt der Empfänger unauflösend. 
    
Wenn ein oder mehrere Empfänger nicht aufgelöst sind, gibt **ResolveName** MAPI_E_NOT_FOUND zurück. Wenn mindestens ein Empfänger eine mehrdeutige Auflösung aufwies, die nicht mit einem Dialogfeld aufgelöst werden konnte oder weil das MAPI_DIALOG-Kennzeichen nicht festgelegt wurde, gibt **ResolveName** MAPI_E_AMBIGUOUS_RECIP zurück. Wenn einige der Empfänger mehrdeutig sind und einige nicht aufgelöst werden können, kann **ResolveName** einen der beiden Fehlerwerte zurückgeben. 
  
Wenn ein Name nicht aufgelöst werden kann, kann der Client eine einmalige Adresse mit einer speziell formatierten Adresse und Eintrags-ID erstellen. Weitere Informationen zum Format von einmaligen Eintragsbezeichnern finden Sie unter ["One-Off Entry Identifiers".](one-off-entry-identifiers.md) Weitere Informationen zum Format von einmaligen Adressen finden Sie unter ["Einmalige Adressen".](one-off-addresses.md)
  
MAPI unterstützt Unicode-Zeichenzeichenfolgen für die **ADRLIST** und die neuen Eintragstitelparameter für **ResolveName**; Wenn Sie das flag MAPI_UNICODE festlegen, werden die folgenden Eigenschaften als Typ PT_UNICODE in den [ADRENTRY-Strukturen](adrentry.md) zurückgegeben: 
  
- **PR_ADDRTYPE** ([PidTagAddressType](pidtagaddresstype-canonical-property.md))
    
- **PR_DISPLAY_NAME** ([PidTagDisplayName](pidtagdisplayname-canonical-property.md))
    
- **PR_EMAIL_ADDRESS** ([PidTagEmailAddress](pidtagemailaddress-canonical-property.md))
    
- **PR_TRANSMITABLE_DISPLAY_NAME** ([PidTagTransmittableDisplayName](pidtagtransmittabledisplayname-canonical-property.md))
    
Die **eigenschaft PR_7BIT_DISPLAY_NAME** ([PidTag7BitDisplayName](pidtag7bitdisplayname-canonical-property.md)) wird jedoch immer als Typ PT_STRING8 zurückgegeben.
  
## <a name="mfcmapi-reference"></a>MFCMAPI-Referenz

Einen MFCMAP-Beispielcode finden Sie in der folgenden Tabelle.
  
|**Datei**|**Funktion**|**Comment**|
|:-----|:-----|:-----|
|MAPIABFunctions.cpp  <br/> |AddOneOffAddress  <br/> |MFCMAPI verwendet die **ResolveName-Methode,** um eine einmalige Adresse aufzulösen, bevor sie einer Nachricht hinzugefügt wird.  <br/> |
|MAPIABFunctions.cpp  <br/> |AddRecipient  <br/> |MFCMAPI verwendet die **ResolveName-Methode,** um einen Adressbucheintrag anhand des Anzeigenamens nachzuschlagen.  <br/> |
   
## <a name="see-also"></a>Siehe auch



[ADRLIST](adrlist.md)
  
[IABContainer::ResolveNames](iabcontainer-resolvenames.md)
  
[IAddrBook::Address](iaddrbook-address.md)
  
[IAddrBook : IMAPIProp](iaddrbookimapiprop.md)


[MFCMAPI (engl.) als ein Codebeispiel](mfcmapi-as-a-code-sample.md)

