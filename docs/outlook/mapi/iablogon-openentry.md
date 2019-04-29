---
title: IABLogonOpenEntry
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- IABLogon.OpenEntry
api_type:
- COM
ms.assetid: 1cfb82f7-5215-4faa-af25-5b1da7e31209
description: 'Letzte Änderung: Samstag, 23. Juli 2011'
ms.openlocfilehash: 70f61ef553350f08eed96c1ee4e9ab790359d1fc
ms.sourcegitcommit: 8657170d071f9bcf680aba50b9c07f2a4fb82283
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 04/28/2019
ms.locfileid: "33409230"
---
# <a name="iablogonopenentry"></a>IABLogon::OpenEntry

  
  
**Gilt für**: Outlook 2013 | Outlook 2016 
  
Öffnet einen Container, einen Messagingbenutzer oder eine Verteilerliste und gibt einen Zeiger auf eine Schnittstellenimplementierung zurück, um weiteren Zugriff zu ermöglichen.
  
```cpp
HRESULT OpenEntry(
  ULONG cbEntryID,
  LPENTRYID lpEntryID,
  LPCIID lpInterface,
  ULONG ulFlags,
  ULONG FAR * lpulObjType,
  LPUNKNOWN FAR * lppUnk
);
```

## <a name="parameters"></a>Parameter

 _cbEntryID_
  
> in Die Anzahl der Bytes in der Eintrags-ID, auf die durch den _lpEntryID_ -Parameter verwiesen wird. 
    
 _lpEntryID_
  
> in Ein Zeiger auf die Eintrags-ID des Containers, des Messaging Benutzers oder der Verteilerliste, die geöffnet werden soll.
    
 _lpInterface_
  
> in Ein Zeiger auf die Schnittstellen-ID (IID), die die Schnittstelle darstellt, die für den Zugriff auf das Open-Objekt verwendet werden soll. Beim Übergeben von NULL wird der Bezeichner für die Standardschnittstelle des Objekts zurückgegeben. Für Container ist die Standardschnittstelle [IABContainer: IMAPIContainer](iabcontainerimapicontainer.md). Die Standardschnittstellen für Adressbuch Objekte sind [IDistList: IMAPIContainer](idistlistimapicontainer.md) für eine Verteilerliste und [IMailUser: IMAPIProp](imailuserimapiprop.md) für einen Messagingbenutzer. 
    
 _ulFlags_
  
> in Eine Bitmaske von Flags, die steuert, wie das Objekt geöffnet wird. Die folgenden Flags können festgelegt werden:
    
MAPI_BEST_ACCESS 
  
> Fordert, dass das Objekt mit den maximal zulässigen Netzwerkberechtigungen für den Benutzer und dem maximalen Zugriff auf Clientanwendungen geöffnet wird. Wenn der Client beispielsweise über Lese-/Schreibzugriff verfügt, sollte das Objekt mit Lese-/Schreibzugriff geöffnet werden. Wenn der Client schreibgeschützte Berechtigung hat, sollte das Objekt mit Leseberechtigung geöffnet werden.
    
MAPI_DEFERRED_ERRORS 
  
> Ermöglicht die **** erfolgreiche Rückgabe der OpenEntry-Methode, bevor der aufrufende Client vollständig auf das Objekt zugegriffen hat. Wenn auf das Objekt nicht zugegriffen wird, kann durch einen nachfolgenden Objektaufruf ein Fehler ausgelöst werden. 
    
MAPI_MODIFY 
  
> Fordert Lese-/Schreibzugriff-Berechtigung an. Standardmäßig werden Objekte mit Schreibschutz geöffnet, und Clients sollten nicht davon ausgehen, dass Lese-/Schreibzugriff erteilt wurde.
    
 _lpulObjType_
  
> Out Ein Zeiger auf den Typ des geöffneten Objekts.
    
 _lppUnk_
  
> Out Ein Zeiger auf einen Zeiger auf das geöffnete Objekt.
    
## <a name="remarks"></a>Bemerkungen

S_OK 
  
> Das Objekt wurde erfolgreich geöffnet.
    
MAPI_E_NO_ACCESS 
  
> Entweder hat der Benutzer unzureichende Berechtigungen zum Öffnen des Objekts oder es wurde versucht, ein schreibgeschütztes Objekt mit Lese-/Schreibzugriff zu öffnen.
    
MAPI_E_NOT_FOUND 
  
> Die durch _lpEntryID_ angegebene Eintrags-ID stellt kein Objekt dar. 
    
MAPI_E_UNKNOWN_ENTRYID 
  
> Die Eintrags-ID im _lpEntryID_ -Parameter weist kein vom Adressbuchanbieter erkanntes Format auf. 
    
## <a name="remarks"></a>Bemerkungen

MAPI Ruft die **OpenEntry** -Methode auf, um einen Container, einen Messagingbenutzer oder eine Verteilerliste zu öffnen. 
  
## <a name="notes-to-implementers"></a>Hinweise für Implementierer

Bevor MAPI Ihre **OpenEntry** -Methode aufruft, bestimmt Sie, dass die Eintrags-ID im _lpEntryID_ -Parameter zu Ihnen gehört und nicht zu einem anderen Anbieter. MAPI bewirkt dies, indem die [MAPIUID](mapiuid.md) -Struktur in der Eintrags-ID mit dem **MAPIUID** abgeglichen wird, den Sie durch Aufrufen der [IMAPISupport:: SetProviderUID](imapisupport-setprovideruid.md) -Methode beim Start registriert haben. 
  
Öffnen Sie das Objekt schreibgeschützt, es sei denn, das MAPI_MODIFY-oder MAPI_BEST_ACCESS-Flag wird im _ulFlags_ -Parameter festgelegt. Wenn Sie keine Änderung für das angeforderte Objekt zulassen, öffnen Sie das Objekt nicht, und geben Sie MAPI_E_NO_ACCESS zurück. 
  
Wenn MAPI für _LPENTRYID_NULL übergibt, öffnen Sie den Stammcontainer in der Containerhierarchie.
  
Das Objekt, das Sie öffnen möchten, kann ein Objekt sein, das von einem anderen Anbieter kopiert wurde. In diesem Fall wird die **PR_TEMPLATEID** ([pidtagtemplateid (](pidtagtemplateid-canonical-property.md))-Eigenschaft unterstützt. Wenn das Objekt diese Eigenschaft unterstützt, rufen Sie die [IMAPISupport::](imapisupport-opentemplateid.md) opentemplatecode-Methode auf, um an Code für diesen Eintrag im fremden Anbieter zu binden, übergeben Sie **PR_TEMPLATEID** im _lpTemplateID_ -Parameter und 0 in der _ulTemplateFlags _-Parameter. **IMAPISupport::** opentemplatecode übergibt diese Informationen an den fremden Anbieter in einem Aufruf der [IABLogon::](iablogon-opentemplateid.md) opentemplated-Methode des fremden Anbieters. Wenn **IMAPISupport::** opentemplatecode einen Fehler auslöst, in der Regel, weil der fremde Anbieter nicht verfügbar ist oder nicht im Profil enthalten ist, versuchen Sie, den ungebundenen Eintrag als schreibgeschützt zu behandeln. Weitere Informationen zum Öffnen von Einträgen für fremde Adressbücher finden Sie unter [fungieren als Host-Adressbuchanbieter](acting-as-a-host-address-book-provider.md).
  
## <a name="see-also"></a>Siehe auch



[IABLogon : IUnknown](iablogoniunknown.md)

