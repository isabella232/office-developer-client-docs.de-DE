---
title: IABContainerCreateEntry
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
ms.localizationpriority: medium
api_name:
- IABContainer.CreateEntry
api_type:
- COM
ms.assetid: ea1daf74-d9e3-4304-bf5d-889afeea6ae9
description: 'Letzte Änderung: Samstag, 23. Juli 2011'
ms.openlocfilehash: c24adf9f25ab1d8137de76b84b2f612a45b7090e
ms.sourcegitcommit: a1d9041c20256616c9c183f7d1049142a7ac6991
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 09/24/2021
ms.locfileid: "59616950"
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
  
> [in] Die Anzahl der Bytes im Eintragsbezeichner, auf die der  _lpEntryID-Parameter_ verweist. 
    
 _lpEntryID_
  
> [in] Ein Zeiger auf den Eintragsbezeichner einer Vorlage zum Erstellen neuer Einträge eines bestimmten Typs. 
    
 _ulCreateFlags_
  
> [in] Eine Bitmaske mit Flags, die steuert, wie die Erstellung von Eingaben durchgeführt wird. Die folgenden Flags können festgelegt werden:
    
CREATE_CHECK_DUP_LOOSE 
  
> Eine lose Ebene der Duplikat-Eintragsüberprüfung sollte durchgeführt werden. Die Implementierung der Prüfung auf lose duplizierte Einträge ist anbieterspezifisch. Beispielsweise kann ein Anbieter eine lose Übereinstimmung als zwei Einträge mit demselben Anzeigenamen definieren.
    
CREATE_CHECK_DUP_STRICT 
  
> Es sollte eine strenge Überprüfung der doppelten Einträge durchgeführt werden. Die Implementierung der strengen Doppelten Eintragsüberprüfung ist anbieterspezifisch. Beispielsweise kann ein Anbieter eine strenge Übereinstimmung als zwei Einträge definieren, die sowohl denselben Anzeigenamen als auch die gleiche Messagingadresse aufweisen.
    
CREATE_REPLACE 
  
> Ein neuer Eintrag sollte einen vorhandenen Eintrag ersetzen, wenn festgestellt wird, dass die beiden Duplikate sind.
    
 _lppMAPIPropEntry_
  
> [out] Ein Zeiger auf einen Zeiger auf den neu erstellten Eintrag.
    
## <a name="return-value"></a>Rückgabewert

S_OK 
  
> Der neue Eintrag wurde erfolgreich erstellt.
    
## <a name="remarks"></a>Bemerkungen

Die **IABContainer::CreateEntry-Methode** erstellt einen neuen Eintrag eines bestimmten Typs im angegebenen Container und gibt einen Zeiger auf eine Schnittstellenimplementierung zurück, um weiteren Zugriff auf den Eintrag zu erhalten. Der neue Eintrag wird mithilfe einer Vorlage erstellt, die aus der Liste der verfügbaren Vorlagen des Containers ausgewählt wurde, die in der einmaligen Tabelle veröffentlicht wurden. Aufrufer greifen auf die one-off-Tabelle eines Containers zu, indem sie ihre [IMAPIProp::OpenProperty-Methode](imapiprop-openproperty.md) aufrufen und die **eigenschaft PR_CREATE_TEMPLATES** ([PidTagCreateTemplates](pidtagcreatetemplates-canonical-property.md)) anfordern. 
  
## <a name="notes-to-implementers"></a>Hinweise für Implementierer

Alle Container, die die **IABContainer::CreateEntry-Methode** unterstützen, müssen modifizierbar sein. Legen Sie die AB_MODIFIABLE-Kennzeichnung Ihres Containers in der **eigenschaft PR_CONTAINER_FLAGS** ([PidTagContainerFlags](pidtagcontainerflags-canonical-property.md)) fest, um anzugeben, dass sie modifizierbar ist. 
  
Sie sollten alle  _ulCreateFlags-Flags_ unterstützen. Die Interpretation und Verwendung dieser Flags ist jedoch implementierungsspezifisch, d. h., Sie können bestimmen, was die Semantik von CREATE_CHECK_DUP_LOOSE und CREATE_CHECK_DUP_STRICT im Kontext Ihrer Implementierung bedeuten. Wenn Sie nicht ermitteln können oder nicht, ob es sich bei einem Eintrag um ein Duplikat handelt, lassen Sie immer die Erstellung des Eintrags zu. 
  
Einige Anbieter implementieren eine strenge Eintragsüberprüfung, indem sie den Anzeigenamen, die Messagingadresse und den Suchschlüssel in einem Eintrag abgleichen. Andere Anbieter beschränken die Übereinstimmung auf den Anzeigenamen und die Adresse. Die losen Eingabeüberprüfungen werden häufig nur durch Überprüfen des Anzeigenamens implementiert. 
  
## <a name="notes-to-host-address-book-provider-implementers"></a>Hinweise zu Hostadressbuchanbieter-Implementierern

Wenn Ihr Container Einträge aus den Vorlagen anderer Anbieter erstellen kann, sollte Die Implementierung von **CreateEntry** Speicher für einige oder alle Eigenschaften bereitstellen, die den erstellten Einträgen zugeordnet sind. Wenn Sie z. B. Speicher für die **Eigenschaft PR_DETAILS_TABLE** ([PidTagDetailsTable](pidtagdetailstable-canonical-property.md)) eines Eintrags bereitstellen, können Sie das Dialogfeld "Details" generieren, ohne vom fremdanbieter abhängig zu sein. 
  
Wenn Ihr Container Einträge erstellen kann, die die **eigenschaft PR_TEMPLATEID** ([PidTagTemplateid](pidtagtemplateid-canonical-property.md)) unterstützen, muss die Implementierung von **CreateEntry** folgendermaßen vorgehen: 
  
1. Rufen Sie die [IMAPISupport::OpenTemplateID-Methode](imapisupport-opentemplateid.md) auf. **OpenTemplateID** aktiviert den Code des fremdanbieters, damit der Eintrag an den neuen Eintrag gebunden wird, der erstellt wird. Fremdanbieter unterstützen diesen Bindungsprozess, um die Kontrolle über Einträge zu behalten, die aus ihren Vorlagen in den Containern von Hostadressbuchanbietern erstellt wurden. 
    
2. Führen Sie alle erforderlichen Initialisierungen durch, und füllen Sie das neue Objekt mit allen Eigenschaften aus dem Eintrag im Fremdanbieter auf, den das Objekt im  _Parameter lppMAPIPropNew_ von **OpenTemplateID** zurückgegeben hat.
    
Wenn **OpenTemplateID** erfolgreich ist, kopieren Sie die Eigenschaften in die Implementierung, auf die der  _Parameter "lppMAPIPropNew"_ verweist, und nicht direkt auf die Implementierung, auf die der  _Parameter "lpMAPIPropData"_ verweist. Initialisieren Sie den neuen Eintrag für die Offlineverwendung wie jeder andere Eintrag von einem fremden Anbieter. 
  
Wenn **OpenTemplateID** einen Fehler zurückgibt, sollte **CreateEntry** fehlschlagen. Lassen Sie nicht zu, dass der Eintrag erstellt wird. Da der fremde Anbieter Annahmen über die Daten in Ihrem Anbieter treffen kann, erstellen Sie keinen Eintrag mit einem Vorlagenbezeichner, der nicht erfolgreich an den fremden Anbieter gebunden wurde. 
  
## <a name="notes-to-callers"></a>Hinweise für Aufrufer

Wenn **CreateEntry** zurückgegeben wird, können Sie möglicherweise oder nicht sofort auf den Eintragsbezeichner für den neuen Eintrag zugreifen. Einige Adressbuchanbieter stellen sie erst zur Verfügung, nachdem Sie die [IMAPIProp::SaveChanges-Methode](imapiprop-savechanges.md) des neuen Eintrags aufgerufen haben. 
  
Obwohl doppelte Überprüfungsflags als Parameter an **CreateEntry** übergeben werden, tritt der Duplikatüberprüfungsvorgang erst auf, wenn **SaveChanges** aufgerufen wird. Daher werden verwandte Fehler wie MAPI_E_COLLISION, die angeben, dass versucht wurde, einen bereits vorhandenen Eintrag zu erstellen, von **SaveChanges** anstelle von **CreateEntry** zurückgegeben.
  
## <a name="see-also"></a>Siehe auch



[IABContainer::CopyEntries](iabcontainer-copyentries.md)
  
[IMAPIProp::OpenProperty](imapiprop-openproperty.md)
  
[IMAPIProp::SaveChanges](imapiprop-savechanges.md)
  
[PidTagCreateTemplates (kanonische Eigenschaft)](pidtagcreatetemplates-canonical-property.md)
  
[IABContainer : IMAPIContainer](iabcontainerimapicontainer.md)

