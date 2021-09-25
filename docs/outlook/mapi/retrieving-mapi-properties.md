---
title: Abrufen von MAPI-Eigenschaften
manager: soliver
ms.date: 12/07/2015
ms.audience: Developer
ms.localizationpriority: medium
api_type:
- COM
ms.assetid: bd3f9f59-9020-46e6-9560-86a7a0eeca20
description: 'Letzte �nderung: Montag, 7. Dezember 2015'
ms.openlocfilehash: 8c52f8a6768f43190bff86c8fe71c884102a4c91
ms.sourcegitcommit: a1d9041c20256616c9c183f7d1049142a7ac6991
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 09/24/2021
ms.locfileid: "59624314"
---
# <a name="retrieving-mapi-properties"></a>Abrufen von MAPI-Eigenschaften

 
  
**Gilt für**: Outlook 2013 | Outlook 2016 
  
Wenn ein Client oder Dienstanbieter eine Eigenschaft aus einem Objekt abruft, stellt das Objekt den Wert, den Typ und den Bezeichner der Eigenschaft zur Verfügung. 
  
Clients und Dienstanbieter können die Eigenschaften eines Objekts abrufen, indem sie eine der folgenden Aktionen aufrufen:
  
[IMAPIProp::GetProps](imapiprop-getprops.md)
  
[IMAPIProp::OpenProperty](imapiprop-openproperty.md)
  
[HrGetOneProp](hrgetoneprop.md)
  
Die **GetProps-Methode** wird verwendet, um eine oder mehrere Eigenschaften abzurufen, die keine spezielle oder alternative Schnittstelle für den Zugriff benötigen. Dies bedeutet, dass die mit **GetProps verfügbaren** Eigenschaften klein sind, z. B. ganze Zahlen und boolesche Werte. 
  
 **So rufen Sie mehrere Eigenschaften ab**
  
1. Weisen Sie eine [SPropTagArray-Struktur](sproptagarray.md) zu, die groß genug ist, um die Anzahl der abzurufenden Eigenschaften zu speichern. 
    
2. Legen Sie das **cValues-Element** der **SPropTagArray-Struktur** auf die Anzahl der abzurufenden Eigenschaften fest, und legen Sie jedes **aulPropTag-Element** auf den Bezeichner und Typ einer der Zieleigenschaften fest, sofern möglich. Wenn der Typ unbekannt ist, legen Sie ihn auf PT_UNSPECIFIED fest. Wenn sowohl der Typ als auch der Bezeichner unbekannt sind, suchen Sie diese Informationen, indem Sie [IMAPIProp::GetPropList](imapiprop-getproplist.md)aufrufen. **GetPropList** gibt ein Eigenschaftstagarray mit allen unterstützten Eigenschaften des Objekts zurück. Wenn nur ein Eigenschaftenname verfügbar ist, rufen [Sie IMAPIProp::GetIDsFromNames](imapiprop-getidsfromnames.md) auf, um auf den zugeordneten Bezeichner zuzugreifen. 
    
3. Rufen Sie [IMAPIProp::GetProps](imapiprop-getprops.md) auf, um die Eigenschaft oder Eigenschaften zu öffnen. 
    
Die **OpenProperty-Methode** wird verwendet, um größere Eigenschaften zu öffnen, die eine alternative Schnittstelle wie **IStream** oder [IMAPITable](imapitableiunknown.md) für den Zugriff erfordern. **OpenProperty** wird in der Regel zum Öffnen großer Zeichenfolgen-, Binär- und Objekteigenschaften verwendet und kann nur jeweils eine Eigenschaft öffnen. Aufrufer übergeben den Bezeichner der zusätzlichen Schnittstelle, die als einer der Eingabeparameter erforderlich ist. 
  
Zu den gängigen Verwendungsmöglichkeiten von **OpenProperty** gehören das Öffnen **PR_BODY** ([PidTagBody](pidtagbody-canonical-property.md)), die Eigenschaft, die den Textkörper einer textbasierten Nachricht enthält, **PR_ATTACH_DATA_OBJ** ([PidTagAttachDataObject](pidtagattachdataobject-canonical-property.md)), die Eigenschaft, die ein OLE-Objekt oder eine Nachrichtenanlage enthält, und **PR_CONTAINER_CONTENTS** ([PidTagContainerContents](pidtagcontainercontents-canonical-property.md)), die Eigenschaft, die ein Ordner- oder Adressbuchcontainerinhaltsverzeichnis enthält. 
  
Abhängig von der Eigenschaft wird eine andere Schnittstelle von **OpenProperty** angefordert. **IStream**, eine Schnittstelle, die das Lesen und Schreiben von Eigenschaftsdaten als Bytestream ermöglicht, wird in der Regel verwendet, um auf **PR_BODY** zuzugreifen. [Entweder IMessage](imessageimapiprop.md) oder **IStream** kann verwendet werden, um auf **PR_ATTACH_DATA_OBJ** zuzugreifen. Eingebettete Nachrichtenanlagen, bei denen es sich um Standardnachrichten handelt, verwenden **IMessage,** während Nachrichten im TNEF-Format **IStream** verwenden. Da **PR_CONTAINER_CONTENTS** ein Tabellenobjekt ist, wird mit [IMAPITable](imapitableiunknown.md)darauf zugegriffen.
  
 **So rufen Sie die PR_ATTACH_DATA_BIN Eigenschaft einer Anlage ab**
  
1. Rufen Sie die [OpenStreamOnFile-Funktion](openstreamonfile.md) auf, um einen Datenstrom für die Datei zu öffnen. 
    
2. Rufen Sie die [IMAPIProp::OpenProperty-Methode](imapiprop-openproperty.md) der Nachricht auf, um die **PR_ATTACH_DATA_BIN** ([PidTagAttachDataBinary](pidtagattachdatabinary-canonical-property.md)) -Eigenschaft mit der **IStream-Schnittstelle** abzurufen. Legen Sie die Flags MAPI_MODIFY und MAPI_CREATE fest. 
    
3. Weisen Sie eine **STATSTG-Struktur** zu, und übergeben Sie sie in einem Aufruf an die **IStream::Stat-Methode** des Dateidatenstroms, um deren Größe zu bestimmen. Eine weitere Möglichkeit zum Bestimmen der Streamgröße ist das Aufrufen von **IStream::Seek** mit dem Flag STREAM_SEEK_END. 
    
4. Rufen Sie die **IStream::CopyTo-Methode** des Datenstroms auf, um die Daten aus dem Datenstrom der Datei in den Anlagendatenstrom zu kopieren. 
    
5. Wenn der Kopiervorgang abgeschlossen ist, geben Sie beide Datenströme frei, indem Sie ihre **IUnknown::Release-Methoden** aufrufen. 
    
Wenn **IStream** für den Eigenschaftenzugriff verwendet wird, senden einige Dienstanbieter automatisch die Größe der Eigenschaft mit dem Datenstrom zurück. Das Aufrufen von **OpenProperty** mit dem flag MAPI_DEFERRED_ERRORS kann das Öffnen der Eigenschaft und die Rückgabe der Datenstromgröße verzögern. Wenn **IStream::Stat** aufgerufen wird, um diese Größe nach **OpenProperty** mit dem MAPI_DEFERRED_ERRORS Flag abzurufen, wird die Leistung beeinträchtigt, da diese Abfolge von Aufrufen einen zusätzlichen Remoteprozeduraufruf erzwingt. Um leistungseinbußen zu vermeiden, können Clients eine beliebige MAPI-Methode zwischen den Aufrufen von **OpenProperty** und **Stat** aufrufen.
  
Die [HrGetOneProp-Funktion](hrgetoneprop.md) öffnet wie **OpenProperty** jeweils eine Eigenschaft. **HrGetOneProp** sollte nur verwendet werden, wenn das Zielobjekt auf dem lokalen Computer vorhanden ist. Wenn das Zielobjekt nicht lokal verfügbar ist, kann die wiederholte Verwendung von **HrGetOneProp** zu mehreren Remoteprozeduraufrufen und leistungsbeeinträchtigungen führen. 
  
Aufrufer, die mehrere Eigenschaften benötigen, können **Entweder HrGetOneProp** oder **OpenProperty** in einer Schleife aufrufen oder einen Aufruf von **GetProps** ausführen. Das einmalige Aufrufen von **GetProps** ist effizienter. 
  
> [!NOTE]
> Sichere Eigenschaften sind bei anderen Eigenschaften in einem **GetProps-,** **HrGetOneProp-** oder **GetPropList-Aufruf** nicht automatisch verfügbar. Sichere Eigenschaften müssen explizit mithilfe ihrer Eigenschaftenbezeichner angefordert werden. 
  
## <a name="see-also"></a>Siehe auch



[Übersicht über die MAPI-Eigenschaft](mapi-property-overview.md)

