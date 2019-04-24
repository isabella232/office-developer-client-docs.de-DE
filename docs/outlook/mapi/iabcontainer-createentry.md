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
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 04/23/2019
ms.locfileid: "32287028"
---
# <a name="iabcontainercreateentry"></a>IABContainer::CreateEntry

  
  
**Gilt für**: Outlook 2013 | Outlook 2016 
  
Erstellt einen neuen Eintrag, bei dem es sich um einen Messagingbenutzer, eine Verteilerliste oder einen anderen Container handeln kann.
  
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
  
> in Die Anzahl der Bytes in der Eintrags-ID, auf die durch den _lpEntryID_ -Parameter verwiesen wird. 
    
 _lpEntryID_
  
> in Ein Zeiger auf den Eintragsbezeichner einer Vorlage zum Erstellen neuer Einträge eines bestimmten Typs. 
    
 _ulCreateFlags_
  
> in Eine Bitmaske von Flags, die die Ausführung der Eintragserstellung steuert. Die folgenden Flags können festgelegt werden:
    
CREATE_CHECK_DUP_LOOSE 
  
> Es sollte eine Ebene doppelter Eintrags Überprüfung durchgeführt werden. Die Implementierung von Loose Duplicate entry checking ist Anbieter spezifisch. Ein Anbieter kann beispielsweise eine lockere Übereinstimmung als zwei Einträge definieren, die den gleichen Anzeigenamen aufweisen.
    
CREATE_CHECK_DUP_STRICT 
  
> Es sollte eine strenge doppelte Eintrags Überprüfung durchgeführt werden. Die Implementierung einer strengen doppelten Eintrags Überprüfung ist Anbieter spezifisch. Ein Anbieter kann beispielsweise eine strikte Übereinstimmung als zwei Einträge definieren, die den gleichen Anzeigenamen und die gleiche Messaging Adresse aufweisen.
    
CREATE_REPLACE 
  
> Ein neuer Eintrag sollte ein vorhandenes ersetzen, wenn festgestellt wird, dass die beiden Duplikate sind.
    
 _lppMAPIPropEntry_
  
> Out Ein Zeiger auf einen Zeiger auf den neu erstellten Eintrag.
    
## <a name="return-value"></a>Rückgabewert

S_OK 
  
> Der neue Eintrag wurde erfolgreich erstellt.
    
## <a name="remarks"></a>Bemerkungen

Die **IABContainer:: CreateEntry** -Methode erstellt einen neuen Eintrag eines bestimmten Typs im angegebenen Container und gibt einen Zeiger auf eine Schnittstellenimplementierung zurück, um weiteren Zugriff auf den Eintrag zu erhalten. Der neue Eintrag wird mithilfe einer Vorlage erstellt, die aus der Liste der verfügbaren Vorlagen des Containers ausgewählt wurde, die in der einmaligen Tabelle veröffentlicht wurden. Aufrufer greifen auf die einmalige Tabelle eines Containers zu, indem Sie die [IMAPIProp:: OpenProperty](imapiprop-openproperty.md) -Methode aufrufen und die **PR_CREATE_TEMPLATES** ([pidtagcreatetemplates (](pidtagcreatetemplates-canonical-property.md))-Eigenschaft anfordern. 
  
## <a name="notes-to-implementers"></a>Hinweise für Implementierer

Alle Container, die die **IABContainer:: CreateEntry** -Methode unterstützen, müssen geändert werden können. Legen Sie das AB_MODIFIABLE-Flag ihres Containers in seiner **PR_CONTAINER_FLAGS** ([pidtagcontainerflags (](pidtagcontainerflags-canonical-property.md))-Eigenschaft fest, um anzugeben, dass es veränderbar ist. 
  
Sie sollten alle _ulCreateFlags_ -Flags unterstützen. Die Interpretation und Verwendung dieser Flags ist jedoch implementierungsspezifisch, d. h., Sie können bestimmen, welche Semantik von CREATE_CHECK_DUP_LOOSE und CREATE_CHECK_DUP_STRICT im Kontext ihrer Implementierung bedeuten. Wenn Sie nicht oder nicht feststellen können, ob ein Eintrag ein Duplikat ist, dürfen Sie immer den Eintrag erstellen. 
  
Einige Anbieter implementieren strenge Eingabeprüfungen, indem Sie den Anzeigenamen, die Messaging Adresse und den Suchschlüssel in einem Eintrag vergleichen. andere Anbieter begrenzen die Übereinstimmung auf Anzeigename und-Adresse. Die Überprüfung des losen Eintrags wird häufig durch Überprüfen des Anzeigenamens implementiert. 
  
## <a name="notes-to-host-address-book-provider-implementers"></a>Hinweise für Host-Adressbuchanbieter-Implementierer

Wenn Ihr Container Einträge aus den Vorlagen anderer Anbieter erstellen kann, sollte Ihre Implementierung von **CreateEntry** Speicher für einige oder alle Eigenschaften bereitstellen, die den erstellten Einträgen zugeordnet sind. Wenn Sie beispielsweise Speicher für die **PR_DETAILS_TABLE** ([pidtagdetailstable (](pidtagdetailstable-canonical-property.md))-Eigenschaft eines Eintrags bereitstellen, können Sie das Dialogfeld Details generieren, ohne vom fremden Anbieter abhängig zu sein. 
  
Wenn der Container Einträge erstellen kann, die die **PR_TEMPLATEID** ([pidtagtemplateid (](pidtagtemplateid-canonical-property.md))-Eigenschaft unterstützen, **** muss die Implementierung von CreateEntry wie folgt vorgehen: 
  
1. Rufen Sie die [IMAPISupport::](imapisupport-opentemplateid.md) opentemplatecode-Methode auf. **** Opentemplateable aktiviert den Code des fremden Anbieters für den Eintrag, um eine Bindung an den neuen Eintrag zu erstellen, der erstellt wird. Ausländische Anbieter unterstützen diesen Bindungsprozess, um die Kontrolle über Einträge, die aus ihren Vorlagen erstellt wurden, in die Container von Host Adressbuch Anbietern zu erhalten. 
    
2. Führen Sie alle erforderlichen Initialisierungen aus, und füllen Sie das neue Objekt mit allen Eigenschaften aus dem Eintrag im fremden Anbieter, den das Objekt im _lppMAPIPropNew_ -Parameter **** von opentemplatecollection zurückgibt.
    
Wenn **** opentemplatename erfolgreich ist, kopieren Sie die Eigenschaften in die Implementierung, auf die durch den _lppMAPIPropNew_ -Parameter verwiesen wird, statt direkt auf die Implementierung, auf die durch den _lpMAPIPropData_ -Parameter verwiesen wird. Initialisieren Sie den neuen Eintrag für die Offlineverwendung wie jeder andere Eintrag eines fremden Anbieters. 
  
Wenn **** opentemplatecollection einen Fehler zurückgibt, sollte CreateEntry fehlschlagen. **** Lassen Sie den Eintrag nicht erstellen. Da der fremde Anbieter Annahmen über die Daten in Ihrem Anbieter treffen kann, erstellen Sie keinen Eintrag mit einem Vorlagenbezeichner, der nicht erfolgreich an den fremden Anbieter gebunden wurde. 
  
## <a name="notes-to-callers"></a>Hinweise für Aufrufer

Wenn **CreateEntry** zurückgegeben wird, können Sie möglicherweise nicht sofort auf die Eintrags-ID für den neuen Eintrag zugreifen. Einige Adressbuchanbieter stellen Sie erst dann zur Verfügung, wenn Sie die [IMAPIProp:: SaveChanges](imapiprop-savechanges.md) -Methode des neuen Eintrags aufgerufen haben. 
  
Obwohl doppelt überprüfende Kennzeichnungen als Parameter **** an CreateEntry übergeben werden, tritt der Vorgang der doppelten Überprüfung erst auf, wenn **SaveChanges** aufgerufen wird. Daher werden verwandte Fehler wie MAPI_E_COLLISION, die darauf hindeuten, dass ein Versuch unternommen wurde, einen bereits vorhandenen Eintrag zu erstellen, **** von SaveChanges anstelle von CreateEntry zurückgegeben. ****
  
## <a name="see-also"></a>Siehe auch



[IABContainer::CopyEntries](iabcontainer-copyentries.md)
  
[IMAPIProp::OpenProperty](imapiprop-openproperty.md)
  
[IMAPIProp::SaveChanges](imapiprop-savechanges.md)
  
[Kanonische Pidtagcreatetemplates (-Eigenschaft](pidtagcreatetemplates-canonical-property.md)
  
[IABContainer : IMAPIContainer](iabcontainerimapicontainer.md)

