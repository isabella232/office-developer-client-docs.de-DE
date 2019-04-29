---
title: IAddrBookResolveName
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- IAddrBook.ResolveName
api_type:
- COM
ms.assetid: a7823c16-efda-45c2-b931-3e1fbc823b0b
description: 'Letzte Änderung: Montag, 9. März 2015'
ms.openlocfilehash: 8a6a73153b857078cb37d94a634a6b0215a0a8c5
ms.sourcegitcommit: 8657170d071f9bcf680aba50b9c07f2a4fb82283
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 04/28/2019
ms.locfileid: "33408131"
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
  
> in Ein Handle für das übergeordnete Fenster eines Dialogfelds, das angezeigt wird, falls angegeben, um den Benutzer aufzufordern, Mehrdeutigkeiten aufzulösen.
    
 _ulFlags_
  
> in Eine Bitmaske von Flags, die verschiedene Aspekte des Lösungsprozesses steuern. Die folgenden Flags können festgelegt werden:
    
AB_UNICODEUI
  
> Gibt an, dass _lpszNewEntryTitle_ eine Unicode-Zeichenfolge ist. 
    
MAPI_CACHE_ONLY
  
> Verwenden Sie nur das Offlineadressbuch, um die Namensauflösung durchzuführen. Sie können dieses Flag beispielsweise verwenden, um einer Clientanwendung die globale Adressliste (GAL) im Exchange-Cache-Modus zu öffnen und auf einen Eintrag in diesem Adressbuch aus dem Cache zuzugreifen, ohne Datenverkehr zwischen dem Client und dem Server zu erstellen. Dieses Flag wird nur vom Exchange-Adressbuchanbieter unterstützt.
    
MAPI_DIALOG 
  
> Zeigt ein Dialogfeld an, in dem der Benutzer zusätzliche Informationen zur Namensauflösung anfordern können. Wenn dieses Flag nicht festgelegt ist, wird kein Dialogfeld angezeigt. 
    
MAPI_UNICODE 
  
> Gibt an, dass die in der Adressliste zurückgegebenen Eigenschaften vom Typ PT_UNICODE anstelle von PT_STRING8 sein sollen. 
    
 _lpszNewEntryTitle_
  
> in Ein Zeiger auf Text für den Titel des Steuerelements im Dialogfeld, in dem der Benutzer zur Eingabe eines Empfängers aufgefordert wird. Der Titel variiert je nach Empfängertyp. Der _lpszNewEntryTitle_ -Parameter kann NULL sein. 
    
 _lpAdrList_
  
> [in-out] Ein Zeiger auf eine [ADRLIST](adrlist.md) -Struktur, die die Liste der zu lösenden Empfängernamen enthält. Diese **ADRLIST** -Struktur kann von der [IAddrBook:: Address](iaddrbook-address.md) -Methode erstellt werden. 
    
## <a name="return-value"></a>Rückgabewert

S_OK 
  
> Der Prozess der Namensauflösung war erfolgreich.
    
MAPI_E_AMBIGUOUS_RECIP 
  
> Mindestens ein Empfänger im _lpAdrList_ -Parameter entsprach mehr als einem Eintrag im Adressbuch. In der Regel wird dieser Wert zurückgegeben, wenn das MAPI_DIALOG-Flag festgelegt ist, um die Anzeige eines Dialog Felds zu verbieten. 
    
MAPI_E_NOT_FOUND 
  
> Mindestens ein Empfänger im _lpAdrList_ -Parameter kann nicht aufgelöst werden. In der Regel wird dieser Wert zurückgegeben, wenn das MAPI_DIALOG-Flag festgelegt ist, um die Anzeige eines Dialog Felds zu verbieten. 
    
## <a name="remarks"></a>Bemerkungen

Clients und Dienstanbieter rufen die **** ResolveName-Methode auf, um den Prozess der Namensauflösung zu initiieren. Ein nicht aufgelöster Eintrag ist ein Eintrag, der noch nicht über eine Eintrags-ID oder **PR_ENTRYID** ([PidTagEntryId](pidtagentryid-canonical-property.md))-Eigenschaft verfügt.
  
 **** ResolveName durchläuft den folgenden Prozess für jeden nicht aufgelösten Eintrag in der Adressliste, die im _lpAdrList_ -Parameter übergeben wird. 
  
1. Wenn der Adresstyp des Empfängers dem Format einer SMTP-Adresse ( _DisplayName_@ _Domain. Top-Level-Domain_) entspricht, weist ResolveName eine einmalige Eintrags-ID zu. **** 
    
2. Für jeden Container in der **PR_AB_SEARCH_PATH** ([pidtagabsearchpath (](pidtagabsearchpath-canonical-property.md))-Eigenschaft **** ruft ResolveName die [IABContainer:: ResolveNames](iabcontainer-resolvenames.md) -Methode auf. **ResolveNames** versucht, den Anzeigenamen aller nicht aufgelösten Empfänger mit einem Anzeigenamen zu vergleichen, der zu einem der Einträge gehört. 
    
3. Wenn ein Container **ResolveNames**nicht unterstützt, **** schränkt ResolveName die Inhaltstabelle des Containers mithilfe einer **PR_ANR** ([pidtaganr (](pidtaganr-canonical-property.md))-Eigenschaftseinschränkung ein. Diese Einschränkung bewirkt, dass der Container einen "Best Guess"-Typ der Suche ausführt, um einen übereinstimmenden Empfänger zu finden. Alle Container müssen die **PR_ANR** -Eigenschaftseinschränkung unterstützen. 
    
4. Wenn ein Container einen Empfänger zurückgibt, der mehreren Namen **** entspricht, zeigt ResolveName ein Dialogfeld an, wenn das MAPI_DIALOG-Flag festgelegt ist, mit dem der Benutzer den richtigen Namen auswählen kann. 
    
5. Wenn alle Container in der **PR_AB_SEARCH_PATH** -Eigenschaft aufgerufen wurden und keine Übereinstimmung gefunden wurde, bleibt der Empfänger nicht aufgelöst. 
    
Wenn ein oder mehrere Empfänger nicht aufgelöst werden, gibt **** ResolveName MAPI_E_NOT_FOUND zurück. Wenn ein oder mehrere Empfänger eine mehrdeutige Auflösung hatten, die nicht mit einem Dialogfeld aufgelöst werden konnte, oder weil das MAPI_DIALOG-Flag **** nicht festgelegt wurde, gibt ResolveName MAPI_E_AMBIGUOUS_RECIP zurück. Wenn einige der Empfänger mehrdeutig sind und einige nicht aufgelöst werden können, **** kann ResolveName einen der beiden Fehlerwerte zurückgeben. 
  
Wenn ein Name nicht aufgelöst werden kann, kann der Client eine einmalige Adresse erstellen, die eine speziell formatierte Adress-und Eintrags-ID aufweist. Weitere Informationen zum Format von einmaligen Eintrags Bezeichnern finden Sie unter [einmalige Eintrags-IDs](one-off-entry-identifiers.md). Weitere Informationen zum Format von einmaligen Adressen finden Sie unter [einmalige Adressen](one-off-addresses.md).
  
MAPI unterstützt Unicode-Zeichenfolgen für die **ADRLIST** und die neuen Parameter für den Eintragstitel, um den Namen aufzulösen. **** Wenn Sie das MAPI_UNICODE-Flag festlegen, werden die folgenden Eigenschaften in den PT_UNICODE-Strukturen [](adrentry.md) als Typ zurückgegeben: 
  
- **PR_ADDRTYPE** ([Pidtagaddresstype (](pidtagaddresstype-canonical-property.md))
    
- **PR_DISPLAY_NAME** ([PidTagDisplayName](pidtagdisplayname-canonical-property.md))
    
- **PR_EMAIL_ADDRESS** ([PidTagEmailAddress](pidtagemailaddress-canonical-property.md))
    
- **PR_TRANSMITABLE_DISPLAY_NAME** ([Pidtagtransmittabledisplayname (](pidtagtransmittabledisplayname-canonical-property.md))
    
Die **PR_7BIT_DISPLAY_NAME** ([pidtag7bitdisplayname (](pidtag7bitdisplayname-canonical-property.md))-Eigenschaft wird jedoch immer als Typ PT_String8 zurückgegeben.
  
## <a name="mfcmapi-reference"></a>MFCMAPI-Referenz

Einen MFCMAP-Beispielcode finden Sie in der folgenden Tabelle.
  
|**Datei**|**Funktion**|**Comment**|
|:-----|:-----|:-----|
|MAPIABFunctions. cpp  <br/> |AddOneOffAddress  <br/> |MFCMAPI verwendet die **** ResolveName-Methode, um eine einmalige Adresse aufzulösen, bevor Sie einer Nachricht hinzugefügt wird.  <br/> |
|MAPIABFunctions. cpp  <br/> |AddRecipient  <br/> |MFCMAPI verwendet die **** ResolveName-Methode, um einen Adressbucheintrag anhand des Anzeigenamens zu suchen.  <br/> |
   
## <a name="see-also"></a>Siehe auch



[ADRLIST](adrlist.md)
  
[IABContainer::ResolveNames](iabcontainer-resolvenames.md)
  
[IAddrBook::Address](iaddrbook-address.md)
  
[IAddrBook : IMAPIProp](iaddrbookimapiprop.md)


[MFCMAPI (engl.) als ein Codebeispiel](mfcmapi-as-a-code-sample.md)

