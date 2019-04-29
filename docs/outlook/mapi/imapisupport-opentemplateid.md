---
title: IMAPISupportOpenTemplateID
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- IMAPISupport.OpenTemplateID
api_type:
- COM
ms.assetid: 532f7af0-b2cc-49dd-b1de-e3ec1dc9a3e7
description: 'Letzte Änderung: Samstag, 23. Juli 2011'
ms.openlocfilehash: 07aa508b473f4a87d5b4909f83771549c301a600
ms.sourcegitcommit: 8657170d071f9bcf680aba50b9c07f2a4fb82283
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 04/28/2019
ms.locfileid: "33418505"
---
# <a name="imapisupportopentemplateid"></a>IMAPISupport::OpenTemplateID

  
  
**Gilt für**: Outlook 2013 | Outlook 2016 
  
Öffnet einen Empfängereintrag in einem fremden Adressbuchanbieter.
  
```cpp
HRESULT OpenTemplateID(
ULONG cbTemplateID,
LPENTRYID lpTemplateID,
ULONG ulTemplateFlags,
LPMAPIPROP lpMAPIPropData,
LPCIID lpInterface,
LPMAPIPROP FAR * lppMAPIPropNew,
LPMAPIPROP lpMAPIPropSibling
);
```

## <a name="parameters"></a>Parameter

 _cbTemplateID_
  
> in Die Anzahl der Bytes im Vorlagenbezeichner, auf die von _lpTemplateID_verwiesen wird. 
    
 _lpTemplateID_
  
> in Ein Zeiger auf die **PR_TEMPLATEID** ([pidtagtemplateid (](pidtagtemplateid-canonical-property.md))-Eigenschaft der Vorlagen-ID des zu öffnenden Empfänger Eintrags.
    
 _ulTemplateFlags_
  
> in Eine Bitmaske von Flags, die zum Öffnen des Eintrags verwendet wird. Das folgende Flag kann festgelegt werden:
    
FILL_ENTRY 
  
> Es wird ein neuer Eintrag erstellt. Wenn der fremde Anbieter den folgenden [IABLogon::](iablogon-opentemplateid.md) opentemplater-Aufruf von MAPI erhält, kann er steuern, wie der Eintrag erstellt wird, indem Eigenschaften geändert werden, auf die durch den _lpMAPIPropData_ -Parameter verwiesen wird, oder indem eine bestimmte Schnittstelle zurückgegeben wird. Implementierung in _lppMAPIPropNew_ , um zu steuern, wie Eigenschaften für den neuen Eintrag festgelegt werden. 
    
 _lpMAPIPropData_
  
> in Ein Zeiger auf die Schnittstellenimplementierung, die der Aufrufer für den Zugriff auf den Eintrag verwendet. Dies ist die Implementierung, die der fremde Anbieter mit seiner eigenen Implementierung umschließen und im _lppMAPIPropNew_ -Parameter zurückgeben kann. Der _lpMAPIPropData_ -Parameter muss auf eine Lese-/Schreibzugriff-Schnittstellenimplementierung verweisen, die von [IMAPIProp: IUnknown](imapipropiunknown.md) abgeleitet ist und die Schnittstelle unterstützt, die im _lpInterface_ -Parameter angefordert wird. 
    
 _lpInterface_
  
> in Ein Zeiger auf die Schnittstellen-ID (IID), die die Schnittstelle darstellt, die für den Zugriff auf den Eintrag verwendet werden soll. Der _lppMAPIPropNew_ -Parameter verweist auf eine Schnittstelle des durch _lpInterface_angegebenen Typs. Beim Übergeben von NULL wird die Standardschnittstelle für einen Messagingbenutzer IID_IMailUser zurückgegeben. 
    
 _lppMAPIPropNew_
  
> Out Ein Zeiger auf die Schnittstellenimplementierung, die der ausländische Anbieter für den Zugriff auf den Eintrag bereitstellt.
    
 _lpMAPIPropSibling_
  
> Reserviert muss NULL sein.
    
## <a name="return-value"></a>Rückgabewert

S_OK 
  
> Der Bindungsprozess war erfolgreich.
    
MAPI_E_UNKNOWN_ENTRYID 
  
> Der fremden Adressbuchanbieter ist nicht vorhanden.
    
## <a name="remarks"></a>Bemerkungen

Die **IMAPISupport::** opentemplatecode-Methode wird nur für Support Objekte des Adressbuch Anbieters implementiert. **** Opentemplatecode wird nur von Adressbuch Anbietern aufgerufen, die als Hosts für Einträge fungieren, die zu anderen Adressbuch Anbietern gehören, auch als ausländische Anbieter bezeichnet. Host Anbieter rufen **** opentemplatecode auf, um einen fremden Eintrag zu öffnen, der auftritt, wenn Daten im Hostanbieter an Code im fremden Anbieter gebunden sind. 
  
## <a name="notes-to-callers"></a>Hinweise für Aufrufer

Rufen **** Sie opentemplatecode nur auf, wenn Sie die Speicherung von Einträgen mit Vorlagen Bezeichnern aus fremden Adressbuch Anbietern unterstützen. Durch diese Unterstützung werden zusätzliche Anforderungen an Ihre [IABContainer:: CreateEntry](iabcontainer-createentry.md) -und [IABLogon:: OpenEntry](iablogon-openentry.md) -Implementierungen gestellt. Weitere Informationen finden Sie in den Beschreibungen dieser Methoden und [fungieren als Host-Adressbuchanbieter](acting-as-a-host-address-book-provider.md).
  
Wenn der **** opentemplatecode-Aufruf als gebundene Schnittstelle die gleiche Property-Objekt-Implementierung zurückgibt, die Sie übergeben haben, können Sie den Verweis auf das Property-Objekt freigeben. Dies liegt daran, dass der Foreign-Anbieter die **AddRef** -Methode des Objekts aufgerufen hat, um seinen eigenen Verweis beizubehalten. Wenn der fremde Anbieter keinen Verweis auf das Property-Objekt beibehalten muss, gibt openTemplatecollection das ungebundene Property-Objekt zurück. **** 
  
Wenn **** opentemplatecode mit MAPI_E_UNKNOWN_ENTRYID fehlschlägt, versuchen Sie, den Eintrag als schreibgeschützt zu verwenden. 
  
## <a name="see-also"></a>Siehe auch



[IABLogon::OpenTemplateID](iablogon-opentemplateid.md)
  
[IPropData: IMAPIProp](ipropdataimapiprop.md)
  
[Kanonische Pidtagtemplateid (-Eigenschaft](pidtagtemplateid-canonical-property.md)
  
[IMAPISupport: IUnknown](imapisupportiunknown.md)

