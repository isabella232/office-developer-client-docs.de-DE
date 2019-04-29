---
title: Abrufen von MAPI-Eigenschaften
manager: soliver
ms.date: 12/07/2015
ms.audience: Developer
localization_priority: Normal
api_type:
- COM
ms.assetid: bd3f9f59-9020-46e6-9560-86a7a0eeca20
description: 'Letzte �nderung: Montag, 7. Dezember 2015'
ms.openlocfilehash: 9666c551543cefd12ee8c902db1a2372aab20632
ms.sourcegitcommit: 8657170d071f9bcf680aba50b9c07f2a4fb82283
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 04/28/2019
ms.locfileid: "33417084"
---
# <a name="retrieving-mapi-properties"></a>Abrufen von MAPI-Eigenschaften

 
  
**Gilt für**: Outlook 2013 | Outlook 2016 
  
Wenn ein Client oder Dienstanbieter eine Eigenschaft von einem Objekt abruft, stellt das Objekt den Wert, Typ und Bezeichner der Eigenschaft zur Verfügung. 
  
Clients und Dienstanbieter können die Eigenschaften eines Objekts abrufen, indem Sie eine der folgenden aufrufen:
  
[IMAPIProp::GetProps](imapiprop-getprops.md)
  
[IMAPIProp::OpenProperty](imapiprop-openproperty.md)
  
[HrGetOneProp](hrgetoneprop.md)
  
Die **** GetProps-Methode wird verwendet, um eine oder mehrere Eigenschaften abzurufen, die keine spezielle oder alternative Schnittstelle für den Zugriff benötigen. Dies impliziert, dass die mit getProps verfügbaren Eigenschaften klein sind, wie Ganzzahlen und boolesche Werte. **** 
  
 **So rufen Sie mehrere Eigenschaften ab**
  
1. Reservieren Sie eine [SPropTagArray](sproptagarray.md) -Struktur, die ausreicht, um die Anzahl der abzurufenden Eigenschaften zu speichern. 
    
2. Legen Sie das **cValues** -Element der **SPropTagArray** -Struktur auf die Anzahl der abzurufenden Eigenschaften fest, und legen Sie jedes **aulPropTag** -Element auf den Bezeichner und Typ, sofern möglich, einer der Zieleigenschaften fest. Wenn der Typ unbekannt ist, legen Sie ihn auf PT_UNSPECIFIED. Wenn sowohl der Typ als auch der Bezeichner unbekannt sind, suchen Sie nach diesen Informationen, indem Sie [IMAPIProp::](imapiprop-getproplist.md)getproplist aufrufen. **** Getproplist gibt ein Property-Tag-Array mit allen unterstützten Eigenschaften des Objekts zurück. Wenn nur ein Eigenschaften Name verfügbar ist, rufen Sie [IMAPIProp:: GetIDsFromNames](imapiprop-getidsfromnames.md) auf, um auf den zugeordneten Bezeichner zuzugreifen. 
    
3. Rufen Sie [IMAPIProp::](imapiprop-getprops.md) GetProps auf, um die Eigenschaften zu öffnen. 
    
Die **OpenProperty** -Methode wird verwendet, um größere Eigenschaften zu öffnen, für die eine Alternative Schnittstelle wie **IStream** oder [IMAPITable](imapitableiunknown.md) für Access erforderlich ist. **OpenProperty** wird normalerweise verwendet, um Zeichenfolgen-, Binär-und Objekteigenschaften mit großem Zeichen zu öffnen und nur jeweils eine Eigenschaft zu öffnen. Aufrufer übergeben den Bezeichner der zusätzlichen Schnittstelle, die als einer der Eingabeparameter erforderlich ist. 
  
Zu den gebräuchlichen Verwendungsmöglichkeiten **** von OpenProperty gehört das Öffnen von **PR_BODY** ([pidtagbody (](pidtagbody-canonical-property.md)), die Eigenschaft, die den Textkörper einer Nachrichten enthält, **PR_ATTACH_DATA_OBJ** ([pidtagattachdataobject (](pidtagattachdataobject-canonical-property.md)), die Eigenschaft mit einem OLE-Objekt oder Nachrichtenanlage und **PR_CONTAINER_CONTENTS** ([pidtagcontainercontents (](pidtagcontainercontents-canonical-property.md)), die Eigenschaft, die eine Ordner-oder Adressbuch Container-Inhaltstabelle enthält. 
  
Abhängig von der Eigenschaft wird eine andere Schnittstelle von OpenProperty **** angefordert. **IStream**, eine Schnittstelle, die das Lesen und Schreiben von Eigenschaftsdaten als Datenstrom ermöglicht, wird in der Regel für den Zugriff auf **PR_BODY**verwendet. Für den Zugriff auf **PR_ATTACH_DATA_OBJ**kann entweder [IMessage](imessageimapiprop.md) oder **IStream** verwendet werden. Eingebettete Nachrichtenanlagen, bei denen es sich um Standardnachrichten handelt, verwenden **IMessage** , wohingegen Nachrichten im TNEF-Format **IStream**verwenden. Da **PR_CONTAINER_CONTENTS** ein Table-Objekt ist, wird mit [IMAPITable](imapitableiunknown.md)zugegriffen.
  
 **So rufen Sie die PR_ATTACH_DATA_BIN-Eigenschaft einer Anlage ab**
  
1. Rufen Sie die [OpenStreamOnFile](openstreamonfile.md) -Funktion auf, um einen Stream für die Datei zu öffnen. 
    
2. Rufen Sie die [IMAPIProp:: OpenProperty](imapiprop-openproperty.md) -Methode der Nachricht auf, um die **PR_ATTACH_DATA_BIN** ([pidtagattachdatabinary (](pidtagattachdatabinary-canonical-property.md))-Eigenschaft mit der **IStream** -Schnittstelle abzurufen. Legen Sie sowohl die MAPI_MODIFY-als auch die MAPI_CREATE-Flags fest. 
    
3. Reservieren Sie eine **STATSTG** -Struktur, und führen Sie Sie in einem Aufruf an die **IStream:: stat** -Methode des Dateistreams, um die Größe zu bestimmen. Eine andere Möglichkeit zum Bestimmen der Datenstrom Größe ist das Aufrufen von **IStream:: Seek** mit dem Flag STREAM_SEEK_END. 
    
4. Rufen Sie die **IStream:: CopyTo** -Methode des Streams auf, um die Daten aus dem Stream der Datei in den Anlagendatenstrom zu kopieren. 
    
5. Wenn der Kopiervorgang abgeschlossen ist, veröffentlichen Sie beide Streams, indem Sie Ihre **IUnknown:: Release** -Methoden aufrufen. 
    
Wenn **IStream** für den Eigenschaftenzugriff verwendet wird, senden einige Dienstanbieter die Größe der Eigenschaft automatisch zurück mit dem Stream. Das **** Aufrufen von OpenProperty mit dem MAPI_DEFERRED_ERRORS-Flag kann das Öffnen der Eigenschaft und die Rückgabe der Datenstrom Größe verzögern. Wenn **IStream:: stat** aufgerufen wird, um diese Größe nach **OpenProperty** mit dem MAPI_DEFERRED_ERRORS-Flag abzurufen, wird die Leistung beeinträchtigt, da diese Sequenz von Aufrufen einen zusätzlichen Remoteprozeduraufruf erzwingt. Um die Leistungseinbußen zu vermeiden, können Clients eine beliebige MAPI-Methode zwischen den **** Aufrufen von OpenProperty und **stat**aufrufen.
  
Die [HrGetOneProp](hrgetoneprop.md) -Funktion, **** wie OpenProperty, öffnet jeweils eine Eigenschaft. **HrGetOneProp** sollte nur verwendet werden, wenn das Zielobjekt auf dem lokalen Computer vorhanden ist. Wenn das Zielobjekt nicht lokal verfügbar ist, kann die Verwendung von **HrGetOneProp** mehrmals zu mehreren Remoteprozeduraufrufen und zu einer Leistungsbeeinträchtigung führen. 
  
Aufrufer, die mehrere Eigenschaften benötigen, können entweder **HrGetOneProp** oder **OpenProperty** in einer Schleife aufrufen oder einen Aufruf an **** GetProps ausführen. Das **** einmalige Aufrufen von GetProps ist effizienter. 
  
> [!NOTE]
> Sichere Eigenschaften sind nicht automatisch mit anderen Eigenschaften in einem getProps-, **HrGetOneProp**-oder getproplist-Aufruf verfügbar. **** **** Sichere Eigenschaften müssen explizit mithilfe ihrer Eigenschaftsbezeichner angefordert werden. 
  
## <a name="see-also"></a>Siehe auch



[Übersicht über die MAPI-Eigenschaft](mapi-property-overview.md)

