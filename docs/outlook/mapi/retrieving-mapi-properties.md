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
  
Wenn ein Client oder Dienstanbieter eine Eigenschaft aus einem Objekt abruft, stellt das Objekt den Wert, den Typ und den Bezeichner der Eigenschaft zur Verfügung. 
  
Clients und Dienstanbieter können die Eigenschaften eines Objekts abrufen, indem sie eine der folgenden Aufrufe verwenden:
  
[IMAPIProp::GetProps](imapiprop-getprops.md)
  
[IMAPIProp::OpenProperty](imapiprop-openproperty.md)
  
[HrGetOneProp](hrgetoneprop.md)
  
Die **GetProps-Methode** wird verwendet, um eine oder mehrere Eigenschaften abzurufen, die keine spezielle oder alternative Schnittstelle für den Zugriff benötigen. Dies impliziert, dass die mit **GetProps** verfügbaren Eigenschaften klein sind, z. B. ganze Zahlen und boolesche Werte. 
  
 **So rufen Sie mehrere Eigenschaften ab**
  
1. Weisen Sie [eine SPropTagArray-Struktur](sproptagarray.md) zu, die groß genug ist, um die Anzahl der abzurufenden Eigenschaften zu halten. 
    
2. Legen Sie **das cValues-Element** der **SPropTagArray-Struktur** auf die Anzahl der abzurufenden Eigenschaften und legen Sie jedes **aulPropTag-Element** auf den Bezeichner und nach Möglichkeit den Typ einer der Zieleigenschaften ein. Wenn der Typ unbekannt ist, legen Sie ihn auf PT_UNSPECIFIED. Wenn sowohl der Typ als auch der Bezeichner unbekannt sind, suchen Sie diese Informationen, indem Sie [IMAPIProp::GetPropList aufrufen.](imapiprop-getproplist.md) **GetPropList** gibt ein Eigenschaftentagarray mit allen unterstützten Eigenschaften des Objekts zurück. Wenn nur ein Eigenschaftenname verfügbar ist, rufen [Sie IMAPIProp::GetIDsFromNames](imapiprop-getidsfromnames.md) auf, um auf den zugeordneten Bezeichner zu zugreifen. 
    
3. Rufen [Sie IMAPIProp::GetProps auf,](imapiprop-getprops.md) um die Eigenschaft oder Eigenschaften zu öffnen. 
    
Die **OpenProperty-Methode** wird verwendet, um größere Eigenschaften zu öffnen, für die eine alternative Schnittstelle wie **IStream** oder [IMAPITable für](imapitableiunknown.md) den Zugriff erforderlich ist. **OpenProperty** wird in der Regel zum Öffnen von Eigenschaften für zeichenfolgen- und binäre Zeichen und Objekte verwendet und kann nur eine Eigenschaft gleichzeitig öffnen. Anrufer übergeben den Bezeichner der zusätzlichen Schnittstelle, die als einer der Eingabeparameter erforderlich ist. 
  
Zu den allgemeinen Verwendungen von **OpenProperty** gehören das Öffnen von **PR_BODY** ([PidTagBody](pidtagbody-canonical-property.md)), die Eigenschaft, die den Textkörper einer textbasierten Nachricht enthält, **PR_ATTACH_DATA_OBJ** ([PidTagAttachDataObject](pidtagattachdataobject-canonical-property.md)), die Eigenschaft, die ein #A0 oder eine Nachrichtenanlage enthält, und **PR_CONTAINER_CONTENTS** ([PidTagContainerContents](pidtagcontainercontents-canonical-property.md)), die Eigenschaft, die eine Ordner- oder Adressbuchcontainerinhaltstabelle enthält. 
  
Je nach Eigenschaft wird eine andere Schnittstelle von **OpenProperty angefordert.** **IStream**, eine Schnittstelle, die das Lesen und Schreiben von Eigenschaftsdaten als Bytestrom ermöglicht, wird in der Regel für den Zugriff auf **PR_BODY.** Entweder [IMessage oder](imessageimapiprop.md) **IStream** können für den Zugriff auf **PR_ATTACH_DATA_OBJ.** Eingebettete Nachrichtenanlagen, die Standardnachrichten sind, verwenden **IMessage,** während Nachrichten im TNEF-Format **IStream verwenden.** Da **PR_CONTAINER_CONTENTS** ein Tabellenobjekt ist, wird mit [IMAPITable darauf zugegriffen.](imapitableiunknown.md)
  
 **So rufen Sie die Eigenschaft PR_ATTACH_DATA_BIN Anlage ab**
  
1. Rufen Sie [die OpenStreamOnFile-Funktion](openstreamonfile.md) auf, um einen Datenstrom für die Datei zu öffnen. 
    
2. Rufen Sie die [IMAPIProp::OpenProperty-Methode](imapiprop-openproperty.md) der Nachricht **auf, um** die PR_ATTACH_DATA_BIN ([PidTagAttachDataBinary](pidtagattachdatabinary-canonical-property.md)) -Eigenschaft mit der **IStream-Schnittstelle abzurufen.** Legen Sie sowohl die MAPI_MODIFY als auch MAPI_CREATE ein. 
    
3. Weisen Sie **eine STATSTG-Struktur** zu, und übergeben Sie sie in einem Aufruf an die **IStream::Stat-Methode** des Dateidatenstroms, um deren Größe zu bestimmen. Eine weitere Möglichkeit zum Bestimmen der Streamgröße ist das Aufrufen **von IStream::Seek** mit dem Flag STREAM_SEEK_END. 
    
4. Rufen Sie die **IStream::CopyTo-Methode** des Datenstroms auf, um die Daten aus dem Datenstrom der Datei in den Anlagendatenstrom zu kopieren. 
    
5. Wenn der Kopiervorgang abgeschlossen ist, geben Sie beide Datenströme frei, indem Sie ihre **IUnknown::Release-Methoden** aufrufen. 
    
Wenn **IStream** für den Eigenschaftszugriff verwendet wird, senden einige Dienstanbieter automatisch die Größe der Eigenschaft mit dem Datenstrom zurück. Das **Aufrufen von OpenProperty** mit dem MAPI_DEFERRED_ERRORS kann das Öffnen der Eigenschaft und die Rückgabe der Streamgröße verzögern. Wenn **IStream::Stat** aufgerufen wird, um diese Größe nach **OpenProperty** mit dem MAPI_DEFERRED_ERRORS-Flagsatz abzurufen, wird die Leistung dadurch beeinträchtigen, dass diese Abfolge von Aufrufen einen zusätzlichen Remoteprozeduraufruf erzwingt. Um den Leistungstreffer zu vermeiden, können Clients eine beliebige MAPI-Methode zwischen den Aufrufen von **OpenProperty** und **Stat aufrufen.**
  
Die [HrGetOneProp-Funktion,](hrgetoneprop.md) wie **OpenProperty**, öffnet eine Eigenschaft nach dem anderen. **HrGetOneProp** sollte nur verwendet werden, wenn das Zielobjekt auf dem lokalen Computer vorhanden ist. Wenn das Zielobjekt nicht lokal verfügbar ist, kann die wiederholte Verwendung von **HrGetOneProp** zu mehreren Remoteprozeduraufrufen und leistungsbeeinträchtigungen führen. 
  
Anrufer, die mehrere Eigenschaften benötigen, können **Entweder HrGetOneProp** oder **OpenProperty** in einer Schleife aufrufen oder **getProps** aufrufen. Das **einmale Aufrufen von GetProps** ist effizienter. 
  
> [!NOTE]
> Sichere Eigenschaften sind nicht automatisch mit anderen Eigenschaften in einem **GetProps-,** **HrGetOneProp-** oder **GetPropList-Aufruf verfügbar.** Sichere Eigenschaften müssen explizit mit ihren Eigenschaftenbezeichnern angefordert werden. 
  
## <a name="see-also"></a>Siehe auch



[Übersicht über die MAPI-Eigenschaft](mapi-property-overview.md)

