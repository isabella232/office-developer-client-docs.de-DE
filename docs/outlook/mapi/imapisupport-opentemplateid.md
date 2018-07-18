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
description: 'Letzte �nderung: Samstag, 23. Juli 2011'
ms.openlocfilehash: f99843bcdf3689acad72145a33d6a9804175a413
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 06/11/2018
ms.locfileid: "19792408"
---
# <a name="imapisupportopentemplateid"></a>IMAPISupport::OpenTemplateID

  
  
**Betrifft**: Outlook 
  
Öffnet einen Empfänger Eintrag in einem fremden Adressbuchanbieter.
  
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
  
> [in] Die Byteanzahl von in der Vorlagenbezeichner auf _LpTemplateID_zeigt. 
    
 _lpTemplateID_
  
> [in] Ein Zeiger auf den Vorlagenbezeichner **PR_TEMPLATEID** ([PidTagTemplateid](pidtagtemplateid-canonical-property.md))-Eigenschaft des Empfängers Eintrags geöffnet werden soll.
    
 _ulTemplateFlags_
  
> [in] Eine Bitmaske der Flags verwendet, um den Eintrag öffnen beschrieben. Das folgende Flag kann festgelegt werden:
    
FILL_ENTRY 
  
> Ein neuer Eintrag wird erstellt. Wenn der Anbieter fremde den nachfolgenden [OpenTemplateID](iablogon-opentemplateid.md) Aufruf von MAPI empfängt, können sie steuern, wie der Eintrag erstellt wird, durch Ändern der Eigenschaften auf die durch den Parameter _LpMAPIPropData_ oder durch eine bestimmte Schnittstelle zurückgeben Implementierung in _LppMAPIPropNew_ steuern, wie die Eigenschaften für den neuen Eintrag festgelegt werden. 
    
 _lpMAPIPropData_
  
> [in] Ein Zeiger auf die Implementierung der Schnittstelle, die der Anrufer wird verwendet, um den Eintrag zugreifen. Dies ist die Implementierung, die der fremde Anbieter mit einer eigenen Implementierung umschließen und im Parameter _LppMAPIPropNew_ zurückgeben kann. Der Parameter _LpMAPIPropData_ muss zeigen Sie auf eine Implementierung der Lese-Schreib-Schnittstelle, die von abgeleitet wird [IMAPIProp: IUnknown](imapipropiunknown.md) und unterstützt die Schnittstelle im Parameter _LpInterface_ angefordert wird. 
    
 _lpInterface_
  
> [in] Ein Zeiger auf die Schnittstelle-ID (IID), die die Schnittstelle verwendet werden, um Zugriff auf den Eintrag darstellt. Der Parameter _LppMAPIPropNew_ verweist auf eine Schnittstelle des Typs durch _LpInterface_angegeben. Übergeben von NULL gibt die Standardschnittstelle für ein messaging-Benutzer IID_IMailUser zurück. 
    
 _lppMAPIPropNew_
  
> [out] Ein Zeiger auf die Implementierung, die der fremde Anbieter für den Zugriff auf den Eintrag bereitstellt.
    
 _lpMAPIPropSibling_
  
> Reserviert. NULL muss sein.
    
## <a name="return-value"></a>R�ckgabewert

S_OK 
  
> Der Bindungsprozess war erfolgreich.
    
MAPI_E_UNKNOWN_ENTRYID 
  
> Die foreign-Adressbuchanbieter ist nicht vorhanden.
    
## <a name="remarks"></a>Bemerkungen

Die **IMAPISupport::OpenTemplateID** -Methode ist nur für Address Book Anbieter Unterstützungsobjekte implementiert. **OpenTemplateID** wird nur von adressbuchanbietern implementierte aufgerufen, die als Hosts für Einträge verwendet werden können, die andere adressbuchanbietern implementierte, auch bekannt als fremden Anbietern angehören. Hostanbieter Aufrufen **OpenTemplateID** um einen fremden Eintrag öffnen, in dem tritt auf, wenn Daten in Hostanbieter Code im fremden Anbieter gebunden ist. 
  
## <a name="notes-to-callers"></a>Hinweise für Aufrufer

Rufen Sie **OpenTemplateID** nur, wenn Sie die Speicherung von Einträgen mit Vorlage Bezeichner aus fremden adressbuchanbietern implementierte unterstützen. Eine solche Unterstützung platziert zusätzliche Anforderungen in Ihrer [IABContainer::CreateEntry](iabcontainer-createentry.md) und [IABLogon::OpenEntry](iablogon-openentry.md) Implementierungen. Weitere Informationen finden Sie in den Beschreibungen dieser Methoden und [fungiert als ein Host-Adressbuchanbieter](acting-as-a-host-address-book-provider.md).
  
Wenn der Anruf **OpenTemplateID** als gebundenen Schnittstelle die Implementierung der gleichen Eigenschaft-Objekt, der Sie übergeben zurückgibt, können Sie den Verweis auf Ihre Property-Objekt freigeben. Dies ist, da der fremde Anbieter das Objekt **AddRef** -Methode, um einen eigenen Verweis behalten aufgerufen hat. Wenn der fremde Anbieter keinen Verweis auf das Property-Objekt behalten muss, gibt **OpenTemplateID** ungebundenen Property-Objekt zurück. 
  
Wenn **OpenTemplateID** mit MAPI_E_UNKNOWN_ENTRYID fehlschlägt, versuchen Sie, fortfahren, indem Sie den Eintrag im schreibgeschützten Modus behandelt. 
  
## <a name="see-also"></a>Siehe auch



[IABLogon::OpenTemplateID](iablogon-opentemplateid.md)
  
[IPropData: IMAPIProp](ipropdataimapiprop.md)
  
[PidTagTemplateid (kanonische Eigenschaft)](pidtagtemplateid-canonical-property.md)
  
[IMAPISupport: IUnknown](imapisupportiunknown.md)

