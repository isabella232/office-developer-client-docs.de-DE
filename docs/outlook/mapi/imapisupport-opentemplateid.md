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
  
> [in] Die Byteanzahl in der Vorlagen-ID, auf die _von lpTemplateID verwiesen wird._ 
    
 _lpTemplateID_
  
> [in] Ein Zeiger auf die **Vorlagen-ID PR_TEMPLATEID** ([PidTagTemplateid](pidtagtemplateid-canonical-property.md))-Eigenschaft des zu öffnenden Empfängereintrags.
    
 _ulTemplateFlags_
  
> [in] Eine Bitmaske mit Flags, mit der das Öffnen des Eintrags beschrieben wird. Das folgende Flag kann festgelegt werden:
    
FILL_ENTRY 
  
> Ein neuer Eintrag wird erstellt. Wenn der fremde Anbieter den nachfolgenden [IABLogon::OpenTemplateID-Aufruf](iablogon-opentemplateid.md) von MAPI empfängt, kann er steuern, wie der Eintrag erstellt wird, indem Eigenschaften geändert werden, auf die der  _lpMAPIPropData-Parameter_ verweist, oder indem er eine bestimmte Schnittstellenimplementierung in  _lppMAPIPropNew_ zurück gibt, um zu steuern, wie Eigenschaften für den neuen Eintrag festgelegt werden. 
    
 _lpMAPIPropData_
  
> [in] Ein Zeiger auf die Schnittstellenimplementierung, die der Aufrufer für den Zugriff auf den Eintrag verwendet. Dies ist die Implementierung, die der fremde Anbieter mit einer eigenen Implementierung umschließen und im  _lppMAPIPropNew-Parameter zurückgeben_ kann. Der  _lpMAPIPropData-Parameter_ muss auf eine Lese-/Schreibschnittstellenimplementierung verweisen, die von [IMAPIProp : IUnknown](imapipropiunknown.md) ab leitet und die Schnittstelle unterstützt, die im  _lpInterface-Parameter_ angefordert wird. 
    
 _lpInterface_
  
> [in] Ein Zeiger auf den Schnittstellenbezeichner (Interface Identifier, IID), der die Schnittstelle darstellt, die für den Zugriff auf den Eintrag verwendet werden soll. Der _lppMAPIPropNew-Parameter_ verweist auf eine Schnittstelle des typs, der durch _lpInterface angegeben wird._ Durch Übergeben von NULL wird die Standardschnittstelle für einen Messagingbenutzer IID_IMailUser. 
    
 _lppMAPIPropNew_
  
> [out] Ein Zeiger auf die Schnittstellenimplementierung, die der fremde Anbieter für den Zugriff auf den Eintrag zur Verfügung stellt.
    
 _lpMAPIPropSibling_
  
> Reserviert; muss NULL sein.
    
## <a name="return-value"></a>Rückgabewert

S_OK 
  
> Der Bindungsprozess war erfolgreich.
    
MAPI_E_UNKNOWN_ENTRYID 
  
> Der fremde Adressbuchanbieter ist nicht vorhanden.
    
## <a name="remarks"></a>Hinweise

Die **IMAPISupport::OpenTemplateID-Methode** wird nur für Unterstützungsobjekte des Adressbuchanbieters implementiert. **OpenTemplateID** wird nur von Adressbuchanbietern aufgerufen, die als Hosts für Einträge fungieren können, die zu anderen Adressbuchanbietern gehören, auch als fremde Anbieter bezeichnet. Hostanbieter rufen **OpenTemplateID auf,** um einen fremden Eintrag zu öffnen, der auftritt, wenn Daten im Hostanbieter an Code im fremden Anbieter gebunden sind. 
  
## <a name="notes-to-callers"></a>Hinweise für Aufrufer

Rufen **Sie OpenTemplateID** nur auf, wenn Sie die Speicherung von Einträgen mit Vorlagenbezeichnern von fremden Adressbuchanbietern unterstützen. Diese Unterstützung stellt zusätzliche Anforderungen an Ihre [IABContainer::CreateEntry-](iabcontainer-createentry.md) und [IABLogon::OpenEntry-Implementierungen.](iablogon-openentry.md) Weitere Informationen finden Sie in den Beschreibungen dieser Methoden und [in Acting as a Host Address Book Provider](acting-as-a-host-address-book-provider.md).
  
Wenn der **OpenTemplateID-Aufruf** als gebundene Schnittstelle dieselbe Eigenschaftsobjektimplementierung zurückgibt, die Sie übergeben haben, können Sie Den Verweis auf Ihr Eigenschaftsobjekt los. Dies liegt daran, dass der fremde Anbieter die **AddRef-Methode** des Objekts aufgerufen hat, um einen eigenen Verweis zu behalten. Wenn der fremde Anbieter keinen Verweis auf das Eigenschaftsobjekt behalten muss, gibt **OpenTemplateID** das ungebundene Eigenschaftsobjekt zurück. 
  
Wenn **OpenTemplateID** mit MAPI_E_UNKNOWN_ENTRYID fehlert, versuchen Sie, den Eintrag als schreibgeschützt zu behandeln. 
  
## <a name="see-also"></a>Siehe auch



[IABLogon::OpenTemplateID](iablogon-opentemplateid.md)
  
[IPropData: IMAPIProp](ipropdataimapiprop.md)
  
[PidTagTemplateid (kanonische Eigenschaft)](pidtagtemplateid-canonical-property.md)
  
[IMAPISupport: IUnknown](imapisupportiunknown.md)

