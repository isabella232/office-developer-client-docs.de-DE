---
title: IMAPISupportOpenTemplateID
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
ms.localizationpriority: medium
api_name:
- IMAPISupport.OpenTemplateID
api_type:
- COM
ms.assetid: 532f7af0-b2cc-49dd-b1de-e3ec1dc9a3e7
description: 'Letzte Änderung: Samstag, 23. Juli 2011'
ms.openlocfilehash: 103feb1641f9537b0f521c0bfd6696879603f852
ms.sourcegitcommit: a1d9041c20256616c9c183f7d1049142a7ac6991
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 09/24/2021
ms.locfileid: "59567417"
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
  
> [in] Die Byteanzahl im Vorlagenbezeichner, auf die von  _lpTemplateID_ verwiesen wird. 
    
 _lpTemplateID_
  
> [in] Ein Zeiger auf die Vorlagen-ID **PR_TEMPLATEID** ([PidTagTemplateid](pidtagtemplateid-canonical-property.md)) -Eigenschaft des Empfängereintrags geöffnet werden soll.
    
 _ulTemplateFlags_
  
> [in] Eine Bitmaske mit Flags, die verwendet wird, um zu beschreiben, wie der Eintrag geöffnet wird. Das folgende Kennzeichen kann festgelegt werden:
    
FILL_ENTRY 
  
> Ein neuer Eintrag wird erstellt. Wenn der fremde Anbieter den nachfolgenden [IABLogon::OpenTemplateID-Aufruf](iablogon-opentemplateid.md) von der MAPI empfängt, kann er steuern, wie der Eintrag erstellt wird, indem Eigenschaften geändert werden, auf die durch den  _parameter lpMAPIPropData_ verwiesen wird, oder indem eine bestimmte Schnittstellenimplementierung in  _lppMAPIPropNew_ zurückgegeben wird, um zu steuern, wie Eigenschaften für den neuen Eintrag festgelegt werden. 
    
 _lpMAPIPropData_
  
> [in] Ein Zeiger auf die Schnittstellenimplementierungen, die der Aufrufer für den Zugriff auf den Eintrag verwendet. Dies ist die Implementierung, die der fremde Anbieter mit einer eigenen Implementierung umbrechen und im  _Parameter "lppMAPIPropNew"_ zurückgeben kann. Der  _Parameter lpMAPIPropData_ muss auf eine Schnittstelle mit Lese-/Schreibzugriff verweisen, die von [IMAPIProp : IUnknown](imapipropiunknown.md) abgeleitet ist und die schnittstelle unterstützt, die im  _lpInterface-Parameter_ angefordert wird. 
    
 _lpInterface_
  
> [in] Ein Zeiger auf den Schnittstellenbezeichner (IID), der die Schnittstelle darstellt, die für den Zugriff auf den Eintrag verwendet werden soll. Der  _lppMAPIPropNew-Parameter_ verweist auf eine Schnittstelle des durch  _lpInterface_ angegebenen Typs. Wenn NULL übergeben wird, wird die Standardschnittstelle für einen Messagingbenutzer IID_IMailUser zurückgegeben. 
    
 _lppMAPIPropNew_
  
> [out] Ein Zeiger auf die Schnittstellenimplementierung, die der fremde Anbieter für den Zugriff auf den Eintrag bereitstellt.
    
 _lpMAPIPropSibling_
  
> Reserviert; muss NULL sein.
    
## <a name="return-value"></a>Rückgabewert

S_OK 
  
> Der Bindungsprozess war erfolgreich.
    
MAPI_E_UNKNOWN_ENTRYID 
  
> Der fremde Adressbuchanbieter ist nicht vorhanden.
    
## <a name="remarks"></a>HinwBemerkungeneise

Die **IMAPISupport::OpenTemplateID-Methode** wird nur für Supportobjekte des Adressbuchanbieters implementiert. **OpenTemplateID** wird nur von Adressbuchanbietern aufgerufen, die als Hosts für Einträge fungieren können, die zu anderen Adressbuchanbietern gehören, auch als fremde Anbieter bezeichnet. Hostanbieter rufen **OpenTemplateID** auf, um einen Fremdeintrag zu öffnen, der auftritt, wenn Daten im Hostanbieter an Code im fremden Anbieter gebunden sind. 
  
## <a name="notes-to-callers"></a>Hinweise für Aufrufer

Rufen Sie **OpenTemplateID** nur auf, wenn Sie die Speicherung von Einträgen mit Vorlagenbezeichnern von fremden Adressbuchanbietern unterstützen. Diese Unterstützung stellt zusätzliche Anforderungen an Ihre [IABContainer::CreateEntry-](iabcontainer-createentry.md) und [IABLogon::OpenEntry-Implementierungen.](iablogon-openentry.md) Weitere Informationen finden Sie in den Beschreibungen dieser Methoden und in der [Rolle eines Hostadressbuchanbieters.](acting-as-a-host-address-book-provider.md)
  
Wenn der **OpenTemplateID-Aufruf** als gebundene Schnittstelle die gleiche Eigenschaftsobjektimplementierungen zurückgibt, die Sie übergeben haben, können Sie den Verweis auf Ihr Eigenschaftsobjekt freigeben. Dies liegt daran, dass der fremde Anbieter die **AddRef-Methode** des Objekts aufgerufen hat, um seinen eigenen Verweis beizubehalten. Wenn der fremde Anbieter keinen Verweis auf das Eigenschaftsobjekt beibehalten muss, gibt **OpenTemplateID** das ungebundene Eigenschaftsobjekt zurück. 
  
Wenn **OpenTemplateID** mit MAPI_E_UNKNOWN_ENTRYID fehlschlägt, versuchen Sie fortzufahren, indem Sie den Eintrag als schreibgeschützt behandeln. 
  
## <a name="see-also"></a>Siehe auch



[IABLogon::OpenTemplateID](iablogon-opentemplateid.md)
  
[IPropData: IMAPIProp](ipropdataimapiprop.md)
  
[PidTagTemplateid (kanonische Eigenschaft)](pidtagtemplateid-canonical-property.md)
  
[IMAPISupport: IUnknown](imapisupportiunknown.md)

