---
title: IABContainerCreateEntry
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- IABContainer.CreateEntry
api_type:
- COM
ms.assetid: ea1daf74-d9e3-4304-bf5d-889afeea6ae9
description: 'Letzte Änderung: Samstag, 23. Juli 2011'
ms.openlocfilehash: 9f80130279e3437dd9be947de97d3f0d4181165e
ms.sourcegitcommit: 8657170d071f9bcf680aba50b9c07f2a4fb82283
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 04/28/2019
ms.locfileid: "33411274"
---
# <a name="iabcontainercreateentry"></a>IABContainer::CreateEntry

  
  
**Gilt für**: Outlook 2013 | Outlook 2016 
  
Erstellt einen neuen Eintrag, der ein Messagingbenutzer, eine Verteilerliste oder ein anderer Container sein kann.
  
```cpp
HRESULT CreateEntry(
  ULONG cbEntryID,
  LPENTRYID lpEntryID,
  ULONG ulCreateFlags,
  LPMAPIPROP FAR * lppMAPIPropEntry
);
```

## <a name="parameters"></a>Parameter

 _cbEntryID_
  
> [in] Die Anzahl der Bytes in der Eintrags-ID, auf die der  _lpEntryID-Parameter_ verweist. 
    
 _lpEntryID_
  
> [in] Ein Zeiger auf die Eintrags-ID einer Vorlage zum Erstellen neuer Einträge eines bestimmten Typs. 
    
 _ulCreateFlags_
  
> [in] Eine Bitmaske mit Flags, die steuert, wie die Erstellung von Eingaben ausgeführt wird. Die folgenden Kennzeichen können festgelegt werden:
    
CREATE_CHECK_DUP_LOOSE 
  
> Es sollte eine lose Ebene doppelter Eingabeprüfungen durchgeführt werden. Die Implementierung der Überprüfung von losen doppelten Einträgen ist anbieterspezifisch. Beispielsweise kann ein Anbieter eine lose Übereinstimmung als zwei beliebige Einträge definieren, die denselben Anzeigenamen haben.
    
CREATE_CHECK_DUP_STRICT 
  
> Es sollte eine strenge Stufe doppelter Eingabeprüfungen durchgeführt werden. Die Implementierung einer strengen Doppelten Eintragsprüfung ist anbieterspezifisch. Ein Anbieter kann z. B. eine strikte Übereinstimmung als zwei Einträge definieren, die denselben Anzeigenamen und dieselbe Messagingadresse haben.
    
CREATE_REPLACE 
  
> Ein neuer Eintrag sollte einen vorhandenen Eintrag ersetzen, wenn festgestellt wird, dass es sich bei den beiden um Duplikate handelt.
    
 _lppMAPIPropEntry_
  
> [out] Ein Zeiger auf einen Zeiger auf den neu erstellten Eintrag.
    
## <a name="return-value"></a>Rückgabewert

S_OK 
  
> Der neue Eintrag wurde erfolgreich erstellt.
    
## <a name="remarks"></a>Hinweise

Die **IABContainer::CreateEntry-Methode** erstellt einen neuen Eintrag eines bestimmten Typs im angegebenen Container und gibt einen Zeiger auf eine Schnittstellenimplementierung zurück, um weiteren Zugriff auf den Eintrag zu erhalten. Der neue Eintrag wird mithilfe einer Vorlage erstellt, die aus der Liste der verfügbaren Vorlagen ausgewählt wurde, die in der einzigen Tabelle veröffentlicht wurden. Aufrufer greifen auf die #A0 eines Containers zu, indem sie die [IMAPIProp::OpenProperty-Methode](imapiprop-openproperty.md) aufrufen und die **PR_CREATE_TEMPLATES** ([PidTagCreateTemplates](pidtagcreatetemplates-canonical-property.md)) -Eigenschaft anfordern. 
  
## <a name="notes-to-implementers"></a>Hinweise für Implementierer

Alle Container, die die **IABContainer::CreateEntry-Methode** unterstützen, müssen veränderbar sein. Legen Sie das AB_MODIFIABLE des Containers in der **PR_CONTAINER_FLAGS** ([PidTagContainerFlags](pidtagcontainerflags-canonical-property.md)) -Eigenschaft fest, um anzugeben, dass es veränderbar ist. 
  
Sie sollten alle  _ulCreateFlags-Flags_ unterstützen. Die Interpretation und Verwendung dieser Flags ist jedoch implementierungsspezifisch, d. h. Sie können bestimmen, was die Semantik von CREATE_CHECK_DUP_LOOSE und CREATE_CHECK_DUP_STRICT im Kontext Ihrer Implementierung bedeutet. Wenn Sie nicht ermitteln können oder nicht, ob es sich bei einem Eintrag um ein Duplikat handelt, lassen Sie immer zu, dass der Eintrag erstellt wird. 
  
Einige Anbieter implementieren eine strenge Eintragsprüfung, indem sie den Anzeigenamen, die Messagingadresse und den Suchschlüssel in einem Eintrag abgleichen. Andere Anbieter beschränken die Übereinstimmung auf den Anzeigenamen und die Adresse. Die Überprüfung der losen Eingabe wird häufig implementiert, indem nur der Anzeigename überprüft wird. 
  
## <a name="notes-to-host-address-book-provider-implementers"></a>Hinweise zum Hosten von Adressbuchanbieter-Implementierern

Wenn Ihr Container Einträge aus den Vorlagen anderer Anbieter erstellen kann, sollte Ihre Implementierung von **CreateEntry** Speicher für einige oder alle Eigenschaften bereitstellen, die den erstellten Einträgen zugeordnet sind. Wenn Sie beispielsweise Speicher für die **PR_DETAILS_TABLE** ([PidTagDetailsTable](pidtagdetailstable-canonical-property.md))-Eigenschaft eines Eintrags bereitstellen, können Sie das Dialogfeld Details generieren, ohne vom fremden Anbieter abhängig zu sein. 
  
Wenn Ihr Container Einträge erstellen **kann,** die die PR_TEMPLATEID ([PidTagTemplateid](pidtagtemplateid-canonical-property.md)) -Eigenschaft unterstützen, muss Ihre Implementierung von **CreateEntry** die folgenden Schritte tun: 
  
1. Rufen Sie [die IMAPISupport::OpenTemplateID-Methode](imapisupport-opentemplateid.md) auf. **Mit OpenTemplateID** kann der Code des fremden Anbieters für den Eintrag an den zu erstellenden neuen Eintrag gebunden werden. Fremde Anbieter unterstützen diesen Bindungsprozess, um die Kontrolle über Einträge zu behalten, die aus ihren Vorlagen in den Containern von Host-Adressbuchanbietern erstellt wurden. 
    
2. Führen Sie alle erforderlichen Initialisierungen durch, und füllen Sie das neue Objekt mit allen Eigenschaften aus dem Eintrag im fremden Anbieter auf, den das Objekt im  _lppMAPIPropNew-Parameter_ von **OpenTemplateID** zurückgegeben hat.
    
Wenn **OpenTemplateID** erfolgreich ist, kopieren Sie die Eigenschaften in die Implementierung, auf die der  _lppMAPIPropNew-Parameter_ verweist, anstatt direkt auf die Implementierung zu verweist, auf die der  _lpMAPIPropData-Parameter_ verweist. Initialisieren Sie den neuen Eintrag für die Offlineverwendung, wie bei jedem anderen Eintrag von einem fremden Anbieter. 
  
Wenn **OpenTemplateID** einen Fehler zurückgibt, **sollte CreateEntry** fehlschlagen. Lassen Sie das Erstellen des Eintrags nicht zu. Da der fremde Anbieter Annahmen zu den Daten in Ihrem Anbieter treffen kann, erstellen Sie keinen Eintrag mit einem Vorlagenbezeichner, der nicht erfolgreich an den fremden Anbieter gebunden wurde. 
  
## <a name="notes-to-callers"></a>Hinweise für Aufrufer

Wenn **CreateEntry zurückgegeben** wird, können Sie möglicherweise nicht sofort auf die Eintrags-ID für den neuen Eintrag zugreifen. Einige Adressbuchanbieter stellen sie erst zur Verfügung, nachdem Sie die [IMAPIProp::SaveChanges-Methode des](imapiprop-savechanges.md) neuen Eintrags aufgerufen haben. 
  
Obwohl doppelte Überprüfungskennzeichen als Parameter an **CreateEntry** übergeben werden, tritt der Doppelte Überprüfungsvorgang erst auf, wenn **SaveChanges** aufgerufen wird. Daher werden verwandte Fehler wie MAPI_E_COLLISION, die angeben, dass versucht wurde, einen bereits vorhandenen Eintrag zu erstellen, von **SaveChanges** anstelle von **CreateEntry zurückgegeben.**
  
## <a name="see-also"></a>Siehe auch



[IABContainer::CopyEntries](iabcontainer-copyentries.md)
  
[IMAPIProp::OpenProperty](imapiprop-openproperty.md)
  
[IMAPIProp::SaveChanges](imapiprop-savechanges.md)
  
[PidTagCreateTemplates (kanonische Eigenschaft)](pidtagcreatetemplates-canonical-property.md)
  
[IABContainer : IMAPIContainer](iabcontainerimapicontainer.md)

