---
title: IABLogonPrepareRecips
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
ms.localizationpriority: medium
api_name:
- IABLogon.PrepareRecips
api_type:
- COM
ms.assetid: 3c1845ea-e291-4855-9afd-51d2c64d7e85
description: 'Letzte Änderung: Samstag, 23. Juli 2011'
ms.openlocfilehash: a7a9459a1b3eb83540db9ab11e0bb01e7e6cf9de
ms.sourcegitcommit: a1d9041c20256616c9c183f7d1049142a7ac6991
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 09/24/2021
ms.locfileid: "59584486"
---
# <a name="iablogonpreparerecips"></a>IABLogon::PrepareRecips

**Gilt für**: Outlook 2013 | Outlook 2016 
  
Bereitet eine Empfängerliste für die spätere Verwendung durch das Messagingsystem vor.
  
```cpp
HRESULT PrepareRecips(
  ULONG ulFlags,
  LPSPropTagArray lpPropTagArray,
  LPADRLIST lpRecipList
);
```

## <a name="parameters"></a>Parameter

_ulFlags_
  
> [in] Eine Bitmaske mit Flags, die den Texttyp in den zurückgegebenen Zeichenfolgen steuert. Das folgende Kennzeichen kann festgelegt werden:
    
  - MAPI_CACHE_ONLY: Verwenden Sie nur das Offlineadressbuch, um die Namensauflösung auszuführen. Beispielsweise können Sie dieses Flag verwenden, um einer Clientanwendung das Öffnen der globalen Adressliste (GAL) im Cache-Exchange-Modus und den Zugriff auf einen Eintrag in diesem Adressbuch aus dem Cache zu ermöglichen, ohne Datenverkehr zwischen dem Client und dem Server zu erstellen. Dieses Flag wird nur vom Exchange Adressbuchanbieter unterstützt.
    
_lpPropTagArray_
  
> [in] Ein Zeiger auf eine [SPropTagArray-Struktur,](sproptagarray.md) die ein Array von Eigenschaftstags enthält, die die Eigenschaften angeben, die aktualisiert werden müssen, falls vorhanden. Der  _parameter lpPropTagArray_ kann NULL sein. 
    
_lpRecipList_
  
> [in] Ein Zeiger auf eine [ADRLIST-Struktur,](adrlist.md) die die Empfängerliste enthält. 
    
## <a name="return-value"></a>Rückgabewert

S_OK 
  
> Die Empfängerliste wurde erfolgreich vorbereitet.
    
MAPI_E_NOT_FOUND 
  
> Mindestens einer der Empfänger im  _LpRecipList-Parameter_ ist nicht vorhanden. 
    
## <a name="return-value"></a>Rückgabewert

Ein Client ruft die MAPI [IAddrBook::P repareRecips-Methode](iaddrbook-preparerecips.md) auf, um einen Satz von Eigenschaften für einen oder mehrere Empfänger zu ändern oder neu anzuordnen. Die Empfänger sind möglicherweise Teil der Empfängerliste einer ausgehenden Nachricht. MapI überträgt diesen Aufruf an die **IABLogon::P repareRecips-Methode** eines Adressbuchanbieters. 
  
**IABLogon::P repareRecips** führt vier Hauptaufgaben aus: 
  
- Stellt sicher, dass alle Empfänger in der Adressliste, auf die durch den  _Parameter lpRecipList_ verwiesen wird, über einen langfristigen Eintragsbezeichner verfügen. 
    
- Stellt sicher, dass alle Empfänger über die im Eigenschaftenwertarray angegebenen Eigenschaften verfügen, auf die der  _Parameter lpPropTagArray_ verweist. 
    
- Stellt sicher, dass die Eigenschaften aus dem Eigenschaftenwertarray vor allen anderen Eigenschaften angezeigt werden, die vor dem Aufruf vorhanden waren.
    
- Stellt sicher, dass die Reihenfolge der Eigenschaften in der [ADRENTRY-Struktur](adrentry.md) jedes Empfängers in der **ADRLIST-Struktur** identisch ist wie im Eigenschaftenwertarray. 
    
Die **ADRENTRY-Struktur** im  _lpRecipList-Parameter_ enthält eine **ADRENTRY-Struktur** für jeden Empfänger. Jede **ADRENTRY-Struktur** enthält ein Array von [SPropValue-Strukturen,](spropvalue.md) um die Eigenschaften des Empfängers zu beschreiben. When **IABLogon::P repareRecips** returns, the **SPropValue** structure array for each recipient includes the properties from the  _lpPropTagArray_ followed by the other properties for the recipient. 
  
## <a name="notes-to-implementers"></a>Hinweise für Implementierer

Das Implementieren von **IABLogon::P repareRecips** umfasst das Festlegen von Eigenschaften in einer bestimmten Reihenfolge, das Abrufen von Eigenschaftswerten und das Konvertieren von kurzfristigen Eintragsbezeichnern in langfristige Eintragsbezeichner. Die im  _lpPropTagArray-Parameter_ angeforderten Eigenschaften müssen am Anfang des Eigenschaftenwertarrays stehen, das der **ADRENTRY-Struktur** jedes Empfängers im  _lpRecipList-Parameter_ zugeordnet ist. Wenn keine Werte für diese Eigenschaften vorhanden sind, öffnen Sie den zugeordneten Messagingbenutzer oder die zugeordnete Verteilerliste mithilfe des Eintragsbezeichners, und rufen Sie die fehlenden Eigenschaftswerte ab. 
  
Weisen Sie jede in _lpRecipList_ **übergebene SPropValue-Struktur** separat zu, sodass die Strukturen einzeln freigegeben werden können. Wenn Sie zusätzlichen Speicherplatz für eine **SPropValue-Struktur** zuweisen müssen, z. B. zum Speichern der Daten für eine Zeichenfolgeneigenschaft, verwenden Sie die [MAPIAllocateBuffer-Funktion,](mapiallocatebuffer.md) um zusätzlichen Speicherplatz für das vollständige Eigenschaftswertarray zuzuweisen. Verwenden Sie die [MAPIFreeBuffer-Funktion,](mapifreebuffer.md) um das ursprüngliche Eigenschaftswertarray freizugeben, und verwenden Sie dann die [MAPIAllocateMore-Funktion,](mapiallocatemore.md) um den erforderlichen zusätzlichen Arbeitsspeicher zuzuweisen. 
  
Verwenden Sie das folgende Verfahren, um **IABLogon::P repareRecips** zu implementieren:
  
1. Suchen Sie nach Einträgen im _LpPropTagArray-Parameter._ Wenn das Eigenschaftswertarray leer ist, ist keine Arbeit erforderlich. Gibt einen Erfolgswert zurück. 
    
2. Verarbeiten Sie jeden Empfänger im _lpRecipList-Parameter._ Es gibt ein **ADRENTRY-Strukturelement** für jeden Empfänger in der Liste. Ignorieren Sie die folgenden Empfängertypen: 
    
   - Empfänger ohne Eintragsbezeichner im **rgPropVals-Element** ihrer **ADRENTRY-Struktur** (d. a. nicht aufgelöste Empfänger). 
    
   - Empfänger mit einem Eintragsbezeichner, der nicht zu Ihrem Anbieter gehört. Diese Empfänger werden an einen anderen Adressbuchanbieter übergeben.
    
3. Öffnen Sie den Empfänger, und rufen Sie die Eigenschaften ab, die bereits für den Empfänger festgelegt sind.
    
4. Führen Sie das in der  _lpRecipList_ angegebene Eigenschaftenwertarray mit dem Array der eigenschaften zusammen, die von **GetProps** zurückgegeben werden. Wenn die gleiche Eigenschaft in beiden Eigenschaftsarrays auftritt, verwenden Sie den Wert aus  _lpRecipList_.
    
5. Wenn das  _LpRecipList-Eigenschaftswertarray_ groß genug ist, um alle erforderlichen Eigenschaften aufzunehmen, ersetzen Sie es einfach durch das zusammengeführte Array. Wenn das  _LpRecipList-Eigenschaftswertarray_ nicht groß genug ist, ersetzen Sie es durch ein neu zugeordnetes Array. Stellen Sie sicher, dass das neue Array einen aktualisierten Wert in jedem seiner **cValues-Elemente** aufweist. 
    
6. Wenn Sie eine oder mehrere der Eigenschaften im  _LpPropTagArray-Parameter_ nicht erkennen, legen Sie den Eigenschaftentyp in der **ADRENTRY-Struktur** des Empfängers auf PT_ERROR und den Eigenschaftswert entweder auf MAPI_E_NOT_FOUND oder auf einen anderen Wert fest, der einen spezifischeren Grund für die Nichtverfügbarkeit der Eigenschaft ergibt. Informationen zu PT_ERROR finden Sie unter [Eigenschaftstypen.](property-types.md)
    
> [!NOTE]
> Weisen Sie die **ADRLIST-Struktur,** die an **IABLogon::P repareRecips** übergeben wird, niemals neu zu, oder ändern Sie die Anzahl der Einträge. 
  
## <a name="see-also"></a>Siehe auch

- [ADRLIST](adrlist.md)
- [IMAPIProp::GetProps](imapiprop-getprops.md)
- [PidTagEntryId (kanonische Eigenschaft)](pidtagentryid-canonical-property.md)
- [SPropValue](spropvalue.md)
- [IABLogon : IUnknown](iablogoniunknown.md)

