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
description: 'Letzte �nderung: Samstag, 23. Juli 2011'
ms.openlocfilehash: acf9cee9bf0713b909b0d82fc606b015ac28474e
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 06/11/2018
ms.locfileid: "19791977"
---
# <a name="iabcontainercreateentry"></a>IABContainer::CreateEntry

  
  
**Betrifft**: Outlook 
  
Erstellt einen neuen Eintrag, der ein messaging-Benutzer, eine Verteilerliste oder einen anderen Container sein kann.
  
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
  
> [in] Die Anzahl von Bytes in die Eintrags-ID auf den durch den Parameter _LpEntryID_ verwiesen. 
    
 _lpEntryID_
  
> [in] Ein Zeiger auf die Eintrags-ID eine Vorlage zum Erstellen neuer Einträge eines bestimmten Typs. 
    
 _ulCreateFlags_
  
> [in] Eine Bitmaske aus Flags, die steuert, wie der Eintrag Erstellung ausgeführt wird. Die folgenden Kennzeichen können festgelegt werden:
    
CREATE_CHECK_DUP_LOOSE 
  
> Eine weit Ebene der Überprüfung doppelten Eintrags sollte ausgeführt werden. Die Implementierung der weit doppelter Eintrag Überprüfung ist anbieterspezifisch. Beispielsweise kann ein Anbieter eine niedrigen Übereinstimmung definieren, wie alle zwei Einträge, die den gleichen Namen anzuzeigen.
    
CREATE_CHECK_DUP_STRICT 
  
> Eine strikt Überprüfen doppelter Eintrag sollte ausgeführt werden. Die Implementierung der exakte doppelter Eintrag Überprüfung ist anbieterspezifisch. Ein Anbieter kann beispielsweise eine exakte Übereinstimmung definieren, wie alle zwei Einträge, die beide den gleichen Namen und die messaging-Adresse anzuzeigen.
    
CREATE_REPLACE 
  
> Ein neuer Eintrag sollte eine vorhandene ersetzen, wenn festgestellt wird, dass die beiden Duplikate sind.
    
 _lppMAPIPropEntry_
  
> [out] Ein Zeiger auf einen Zeiger auf den neu erstellten Eintrag.
    
## <a name="return-value"></a>R�ckgabewert

S_OK 
  
> Der neue Eintrag wurde erfolgreich erstellt.
    
## <a name="remarks"></a>Bemerkungen

Die **IABContainer::CreateEntry** -Methode erstellt einen neuen Eintrag eines bestimmten Typs im angegebenen Container, einen Zeiger auf eine schnittstellenimplementierung für den weiteren Zugriff auf den Eintrag zurückgibt. Der neue Eintrag wird erstellt, mithilfe einer Vorlage, die aus dem Container-Liste der verfügbaren Vorlagen in der einmaligen Tabelle veröffentlicht ausgewählt wurde. Anrufer zum Öffnen des Containers einmaligen Tabelle Aufrufen seiner [IMAPIProp::OpenProperty](imapiprop-openproperty.md) -Methode und die Eigenschaft **PR_CREATE_TEMPLATES** ([PidTagCreateTemplates](pidtagcreatetemplates-canonical-property.md)) anfordern. 
  
## <a name="notes-to-implementers"></a>Hinweise für Implementierer

Alle Container, die die **IABContainer::CreateEntry** -Methode unterstützen müssen geändert werden. Festlegen des Containers AB_MODIFIABLE Flag in seiner **PR_CONTAINER_FLAGS** ([PidTagContainerFlags](pidtagcontainerflags-canonical-property.md))-Eigenschaft, um anzugeben, dass es geändert werden kann. 
  
Sie sollten alle Flags _UlCreateFlags_ unterstützen. Die Interpretation und die Verwendung dieser Flags Implementierung ist jedoch bestimmte – d. h., können Sie ermitteln, Bedeutung der Semantik der CREATE_CHECK_DUP_LOOSE und CREATE_CHECK_DUP_STRICT im Zusammenhang mit der Implementierung. Wenn Sie nicht oder nicht bestimmen, ob ein Eintrag vorhanden ist, können Sie immer den Eintrag erstellt werden soll. 
  
Einige Anbieter implementieren strenge Kontrolle durch den Anzeigenamen übereinstimmenden Eintrag messaging-Adresse und Suche Schlüssel in einem Eintrag. andere Anbieter beschränken Sie die Übereinstimmung um Namen und Adresse anzuzeigen. Überprüfung der weit Eintrag wird häufig Mobilgeräts auf nur den Anzeigenamen implementiert. 
  
## <a name="notes-to-host-address-book-provider-implementers"></a>Hinweise für Address Book Anbieterimplementierer hosten

Wenn Ihre Container Einträge aus den Vorlagen von anderen Anbietern erstellen kann, sollte die Implementierung von **CreateEntry** Speicher für einige oder alle erstellten Posten zugeordneten Eigenschaften bereitstellen. Wenn Sie Speicher für einen Eintrag **PR_DETAILS_TABLE** ([PidTagDetailsTable](pidtagdetailstable-canonical-property.md))-Eigenschaft angeben, können Sie beispielsweise das Dialogfeld Details generieren, ohne abhängig von der fremde Anbieter. 
  
Wenn Ihre Container Einträge, die die **PR_TEMPLATEID** ([PidTagTemplateid](pidtagtemplateid-canonical-property.md))-Eigenschaft unterstützen erstellen kann, muss die Implementierung von **CreateEntry** Folgendes ausführen: 
  
1. Rufen Sie die [IMAPISupport::OpenTemplateID](imapisupport-opentemplateid.md) -Methode. **OpenTemplateID** ermöglicht der fremde Anbieter Code für den Eintrag zum Binden an den neuen Eintrag erstellt wird. Foreign Anbieter unterstützt diesen Bindungsvorgang um Kontrolle über die Einträge aus ihrer Vorlagen in die Container der Host von adressbuchanbietern implementierte erstellten erhalten. 
    
2. Führen Sie eine beliebige erforderliche Initialisierung, und füllen Sie das neue Objekt mit allen Eigenschaften aus den Eintrag in der fremden Anbieter, den das Objekt im Parameter _LppMAPIPropNew_ von **OpenTemplateID**zurückgegeben.
    
Wenn **OpenTemplateID** erfolgreich ist, kopieren Sie die Eigenschaften auf die Implementierung auf das durch den Parameter _LppMAPIPropNew_ und nicht direkt an die Implementierung der auf den durch den Parameter _LpMAPIPropData_ verwiesen. Initialisieren Sie den neuen Eintrag für die Offlineverwendung, wie Sie einen anderen Eintrag von einem fremden Anbieter. 
  
Wenn **OpenTemplateID** einen Fehler zurückgibt, sollte **CreateEntry** fehlschlagen. Lassen Sie nicht den Eintrag erstellt werden soll. Da der fremde Anbieter Annahmen über die Daten im Anbieter machen kann, erstellen Sie einen Eintrag nicht mit einer Vorlage-ID, die nicht erfolgreich an den foreign Anbieter gebunden wurde. 
  
## <a name="notes-to-callers"></a>Hinweise für Aufrufer

Wenn **CreateEntry** zurückgibt, Sie oder möglicherweise nicht sofort die Eintrags-ID für den neuen Eintrag zugreifen. Einige adressbuchanbietern implementierte machen nicht es erst verfügbar, nachdem Sie den neuen Eintrag [IMAPIProp::SaveChanges](imapiprop-savechanges.md) -Methode aufgerufen haben. 
  
Obwohl doppelte Überprüfung Flags an **CreateEntry**als Parameter übergeben werden, tritt das Duplikat Überprüfung der Vorgang nicht bis **SaveChanges** aufgerufen wird. Aus diesem Grund werden verwandte Fehler wie MAPI_E_COLLISION, gibt an, dass versucht wurde, einen bereits vorhandenen Eintrag erstellen, von **SaveChanges** statt **CreateEntry**zurückgegeben.
  
## <a name="see-also"></a>Siehe auch



[IABContainer::CopyEntries](iabcontainer-copyentries.md)
  
[IMAPIProp::OpenProperty](imapiprop-openproperty.md)
  
[IMAPIProp::SaveChanges](imapiprop-savechanges.md)
  
[PidTagCreateTemplates (kanonische Eigenschaft)](pidtagcreatetemplates-canonical-property.md)
  
[IABContainer : IMAPIContainer](iabcontainerimapicontainer.md)

