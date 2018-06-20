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
ms.openlocfilehash: 41157b97eb28787deaf19c2e974da23dfb77e0be
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 06/11/2018
ms.locfileid: "19795388"
---
# <a name="retrieving-mapi-properties"></a>Abrufen von MAPI-Eigenschaften

 
  
**Betrifft**: Outlook 
  
Wenn ein Client oder Dienstanbieter aus einem Objekt eine Eigenschaft abruft, stellt das Objekt zur Verfügung, der Wert der Eigenschaft, Type und Bezeichner. 
  
-Clients und -Dienstanbieter können Eigenschaften eines Objekts abrufen, indem Sie eine der folgenden:
  
[IMAPIProp::GetProps](imapiprop-getprops.md)
  
[IMAPIProp::OpenProperty](imapiprop-openproperty.md)
  
[HrGetOneProp](hrgetoneprop.md)
  
Die **GetProps** -Methode wird verwendet, um eine oder mehrere Eigenschaften abzurufen, die nicht über eine spezielle oder alternative Schnittstelle für den Zugriff benötigen. Dies bedeutet, dass die Eigenschaften verfügbar mit **GetProps** klein wie ganzen Zahlen und boolesche Werte. 
  
 **Abrufen mehrerer Eigenschaften**
  
1. Reservieren Sie eine [SPropTagArray](sproptagarray.md) -Struktur groß genug für die Anzahl der Eigenschaften abgerufen werden sollen. 
    
2. Legen Sie das **cValues** Mitglied der **SPropTagArray** -Struktur auf die Anzahl der Eigenschaften abgerufen und jedes Mitglied **AulPropTag** auf das Bezeichner und Typ, wenn möglich, von der Zieleigenschaften festgelegt werden. Wenn der Typ bekannt ist, legen Sie es auf PT_UNSPECIFIED. Wenn der Typ und der Bezeichner nicht bekannt sind, suchen Sie diese Informationen durch Aufrufen von [IMAPIProp::GetPropList](imapiprop-getproplist.md). **GetPropList** gibt ein Array mit allen unterstützten Eigenschaften des Objekts Tag-Eigenschaft zurück. Wenn nur ein Name der Eigenschaft verfügbar ist, rufen Sie [IMAPIProp::GetIDsFromNames](imapiprop-getidsfromnames.md) Zugriff auf den zugeordneten Bezeichner. 
    
3. Rufen Sie [IMAPIProp::GetProps](imapiprop-getprops.md) , um die Eigenschaft oder Eigenschaften zu öffnen. 
    
Die **OpenProperty** -Methode wird verwendet, um größere Eigenschaften zu öffnen, die eine alternative Schnittstelle wie **IStream** oder [IMAPITable](imapitableiunknown.md) Access erfordern. **OpenProperty** wird in der Regel verwendet, um große Zeichenkette, Binär und Objekteigenschaften geöffnet und kann nur eine Eigenschaft zu einem Zeitpunkt geöffnet. Anrufer übergeben Sie den Bezeichner der zusätzliche Schnittstelle, die als eine der Eingabeparameter erforderlich ist. 
  
Einige häufigen Verwendungsmöglichkeiten des **OpenProperty** umfassen das Öffnen von **PR_BODY** ([PidTagBody](pidtagbody-canonical-property.md)), die Eigenschaft, die im Textkörper der textbasierte Nachricht **PR_ATTACH_DATA_OBJ** ([PidTagAttachDataObject](pidtagattachdataobject-canonical-property.md)), die Eigenschaft enthält, die enthält ein OLE-Objekt oder eine Nachricht Anlage und **PR_CONTAINER_CONTENTS** ([PidTagContainerContents](pidtagcontainercontents-canonical-property.md)), die Eigenschaft, die eine Tabelle Ordner oder Adressbuch Container, Inhalt enthält. 
  
Abhängig von der Eigenschaft ist eine andere Schnittstelle auf **OpenProperty**angefordert haben. **IStream**, können Sie Eigenschaftendaten, besteht Lese- / Schreibzugriff als Stream von Bytes, wird in der Regel **PR_BODY**zugreifen. [IMessage](imessageimapiprop.md) oder **IStream** kann verwendet werden, auf **PR_ATTACH_DATA_OBJ**zugreifen. Eingebettete e-Mail-Anlagen, die standard-Nachrichten sind verwenden **IMessage** **IStream**TNEF-Format für Nachrichten verwendet werden. Da **PR_CONTAINER_CONTENTS** ein Table-Objekt ist, wird es mit [IMAPITable](imapitableiunknown.md)zugegriffen.
  
 **Zum Abrufen einer Anlage PR_ATTACH_DATA_BIN-Eigenschaft**
  
1. Aufruf der Funktion [OpenStreamOnFile nicht ausgeführt werden](openstreamonfile.md) , um einen Stream für die Datei zu öffnen. 
    
2. Rufen Sie die Nachricht [IMAPIProp::OpenProperty](imapiprop-openproperty.md) -Methode zum Abrufen der Eigenschaft **PR_ATTACH_DATA_BIN** ([PidTagAttachDataBinary](pidtagattachdatabinary-canonical-property.md)) mit der **IStream** -Schnittstelle. Legen Sie die MAPI_MODIFY und die MAPI_CREATE ist Flags. 
    
3. Ordnen Sie eine **STATSTG** -Struktur zu, und geben Sie ihn in einem Aufruf der Dateidatenstrom **:: Stat** -Methode zum Bestimmen der Größe. Eine weitere Möglichkeit zum Bestimmen der Größe des Datenstroms wird mit dem Flag STREAM_SEEK_END **IStream:: Seek** aufzurufen. 
    
4. Rufen Sie den Stream **:: CopyTo** -Methode, um die Daten aus der Datei-Stream in die Anlagendatenstrom kopieren. 
    
5. Wenn der Kopiervorgang abgeschlossen ist, geben Sie beide Datenströme durch Aufrufen von ihrer **IUnknown** -Methoden. 
    
Wenn **IStream** für den Zugriff auf Eigenschaften verwendet wird, senden Sie einige Dienstanbieter automatisch die Größe der-Eigenschaft mit dem Stream-Objekt zurück. **OpenProperty** mit der MAPI_DEFERRED_ERRORS aufrufen können Kennzeichen für das Öffnen der-Eigenschaft und die Rückgabe der Größe des Datenstroms verzögern. Wenn **:: Stat** aufgerufen wird, um diese Größe abrufen, **OpenProperty** mit der MAPI_DEFERRED_ERRORS flag festgelegt, wird die Leistung beeinträchtigt werden, da diese Folge der Aufrufe ein sehr Remoteprozeduraufruf erzwingt. Clients können zwischen der Anrufe **OpenProperty** und **Stat**jede MAPI-Methode aufrufen, um die Leistungseinbußen zu vermeiden.
  
Die [HrGetOneProp](hrgetoneprop.md) -Funktion wie **OpenProperty**, wird eine Eigenschaft zu einem Zeitpunkt geöffnet. **HrGetOneProp** sollte nur verwendet werden, wenn das Zielobjekt auf dem lokalen Computer vorhanden ist. Wenn das Zielobjekt nicht lokal verfügbar ist, können **HrGetOneProp** wiederholt mehrere Remoteprozeduraufrufe und Leistungseinbußen führen. 
  
Anrufer, die verschiedene Eigenschaften benötigen können **HrGetOneProp** oder **OpenProperty** in einer Schleife aufrufen oder durch Aufrufen von **GetProps**stellen. **GetProps** einmal aufrufen ist effizienter. 
  
> [!NOTE]
> Schützen von Eigenschaften sind nicht automatisch mit anderen Eigenschaften im Gespräch **GetProps**, **HrGetOneProp**oder **GetPropList** verfügbar. Schützen von Eigenschaften müssen explizit mit ihren Eigenschaftenbezeichnern angefordert werden. 
  
## <a name="see-also"></a>Siehe auch



[�bersicht �ber die MAPI-Eigenschaft](mapi-property-overview.md)

