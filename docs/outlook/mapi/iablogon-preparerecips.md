---
title: IABLogonPrepareRecips
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- IABLogon.PrepareRecips
api_type:
- COM
ms.assetid: 3c1845ea-e291-4855-9afd-51d2c64d7e85
description: 'Letzte Änderung: Samstag, 23. Juli 2011'
ms.openlocfilehash: 0a9b88d762ca88cebd6d9acecf06db53a0b778f6
ms.sourcegitcommit: 8657170d071f9bcf680aba50b9c07f2a4fb82283
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 04/28/2019
ms.locfileid: "33423860"
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
  
> [in] Eine Bitmaske mit Flags, die den Texttyp in den zurückgegebenen Zeichenfolgen steuert. Das folgende Flag kann festgelegt werden:
    
  - MAPI_CACHE_ONLY: Verwenden Sie nur das Offlineadressbuch, um die Namensauflösung durchzuführen. Sie können dieses Flag beispielsweise verwenden, um einer Clientanwendung zu ermöglichen, die globale Adressliste (GAL) im Exchange-Cache-Modus zu öffnen und aus dem Cache auf einen Eintrag in diesem Adressbuch zu zugreifen, ohne Datenverkehr zwischen dem Client und dem Server zu erstellen. Dieses Flag wird nur vom adressbuchanbieter Exchange unterstützt.
    
_lpPropTagArray_
  
> [in] Ein Zeiger auf eine [SPropTagArray-Struktur,](sproptagarray.md) die ein Array von Eigenschaftstags enthält, die die Eigenschaften angeben, die gegebenenfalls aktualisiert werden müssen. Der  _lpPropTagArray-Parameter_ kann NULL sein. 
    
_lpRecipList_
  
> [in] Ein Zeiger auf eine [ADRLIST-Struktur,](adrlist.md) die die Empfängerliste enthält. 
    
## <a name="return-value"></a>Rückgabewert

S_OK 
  
> Die Empfängerliste wurde erfolgreich vorbereitet.
    
MAPI_E_NOT_FOUND 
  
> Mindestens einer der Empfänger im  _lpRecipList-Parameter_ ist nicht vorhanden. 
    
## <a name="return-value"></a>Rückgabewert

Ein Client ruft die MAPI [IAddrBook::P repareRecips-Methode](iaddrbook-preparerecips.md) auf, um einen Satz von Eigenschaften für einen oder mehrere Empfänger zu ändern oder neu anzuordnen. Die Empfänger sind möglicherweise Teil der Empfängerliste einer ausgehenden Nachricht. MAPI überträgt diesen Aufruf an die **IABLogon::P repareRecips-Methode eines Adressbuchanbieters.** 
  
**IABLogon::P repareRecips** führt vier Hauptaufgaben aus: 
  
- Stellt sicher, dass alle Empfänger in der Adressliste, auf die der  _lpRecipList-Parameter_ verweist, über einen langfristigen Eintragsbezeichner verfügen. 
    
- Stellt sicher, dass für alle Empfänger die Eigenschaften im Eigenschaftenwertarray angegeben sind, auf die der  _lpPropTagArray-Parameter_ verweist. 
    
- Stellt sicher, dass die Eigenschaften aus dem Eigenschaftswertarray vor allen anderen Eigenschaften angezeigt werden, die vor dem Aufruf vorhanden waren.
    
- Stellt sicher, dass die Reihenfolge der Eigenschaften in der [ADRENTRY-Struktur](adrentry.md) jedes Empfängers in der **ADRLIST-Struktur** mit der reihenfolge im Eigenschaftenwertarray identisch ist. 
    
Die **ADRENTRY-Struktur** im  _lpRecipList-Parameter_ enthält eine **ADRENTRY-Struktur** für jeden Empfänger. Jede **ADRENTRY-Struktur** enthält ein Array von [SPropValue-Strukturen,](spropvalue.md) um die Eigenschaften des Empfängers zu beschreiben. Wenn **IABLogon::P repareRecips** zurückgegeben wird, enthält das **Strukturarray SPropValue** für jeden Empfänger die Eigenschaften aus  _dem lpPropTagArray_ gefolgt von den anderen Eigenschaften für den Empfänger. 
  
## <a name="notes-to-implementers"></a>Hinweise für Implementierer

Die Implementierung von **IABLogon::P repareRecips** umfasst das Festlegen von Eigenschaften in einer bestimmten Reihenfolge, das Abrufen von Eigenschaftswerten und das Konvertieren kurzfristiger Eintragsbezeichner in langfristige Eintragsbezeichner. Die eigenschaften, die im  _lpPropTagArray-Parameter_ angefordert werden, müssen sich am Anfang des Eigenschaftenwertarrays befinden, das der **ADRENTRY-Struktur** jedes Empfängers im  _lpRecipList-Parameter_ zugeordnet ist. Wenn keine Werte für diese Eigenschaften vorhanden sind, öffnen Sie den zugeordneten Messagingbenutzer oder die zugeordnete Verteilerliste mithilfe des Eintragsbezeichners, und rufen Sie die fehlenden Eigenschaftswerte ab. 
  
Weisen Sie jede in _lpRecipList_ **übergebene SPropValue-Struktur** separat zu, damit die Strukturen einzeln frei werden können. Wenn Sie zusätzlichen Speicherplatz für eine **SPropValue-Struktur** zuweisen müssen, z. B. zum Speichern der Daten für eine Zeichenfolgeneigenschaft, verwenden Sie die [MAPIAllocateBuffer-Funktion,](mapiallocatebuffer.md) um zusätzlichen Speicherplatz für das Array mit dem vollständigen Eigenschaftswert zuzuordnen. Verwenden Sie die [MAPIFreeBuffer-Funktion,](mapifreebuffer.md) um das ursprüngliche Eigenschaftswertarray frei zu machen, und verwenden Sie dann die [MAPIAllocateMore-Funktion,](mapiallocatemore.md) um den erforderlichen zusätzlichen Arbeitsspeicher zuzuordnen. 
  
Verwenden Sie das folgende **Verfahren, um IABLogon::P repareRecips** zu implementieren:
  
1. Suchen Sie nach Einträgen im _lpPropTagArray-Parameter._ Wenn das Eigenschaftswertarray leer ist, ist keine Arbeit zu tun. Gibt einen Erfolgswert zurück. 
    
2. Verarbeiten Sie jeden Empfänger im _lpRecipList-Parameter._ Es gibt ein **ADRENTRY-Strukturmitglied** für jeden Empfänger in der Liste. Ignorieren Sie die folgenden Empfängertypen: 
    
   - Empfänger ohne Eintrags-ID im **rgPropVals-Mitglied** ihrer **ADRENTRY-Struktur** (d. h. nicht aufgelöste Empfänger). 
    
   - Empfänger mit einer Eintrags-ID, die nicht zu Ihrem Anbieter gehört. Diese Empfänger werden an einen anderen Adressbuchanbieter übergeben.
    
3. Öffnen Sie den Empfänger, und rufen Sie die Eigenschaften ab, die bereits für den Empfänger festgelegt sind.
    
4. Merge the property value array specified in the  _lpRecipList_ with the array of properties returned from **GetProps**. Wenn die gleiche Eigenschaft in beiden Eigenschaftsarrays auftritt, verwenden Sie den Wert aus  _lpRecipList_.
    
5. Wenn das  _lpRecipList-Eigenschaftswertarray_ groß genug ist, um alle erforderlichen Eigenschaften zu speichern, ersetzen Sie es einfach durch das zusammengeführte Array. Wenn das  _lpRecipList-Eigenschaftswertarray_ nicht groß genug ist, ersetzen Sie es durch ein neu zugewiesenes Array. Stellen Sie sicher, dass das neue Array in jedem seiner **cValues-Elemente einen aktualisierten Wert** hat. 
    
6. Wenn Sie eine oder mehrere Eigenschaften im  _lpPropTagArray-Parameter_ nicht erkennen, legen Sie den Eigenschaftentyp in der **ADRENTRY-Struktur** des Empfängers auf PT_ERROR und den Eigenschaftswert entweder auf MAPI_E_NOT_FOUND oder auf einen anderen Wert fest, der einen genaueren Grund für die Nichtverfügbarkeit der Eigenschaft gibt. Weitere Informationen zu PT_ERROR finden Sie unter [Property Types](property-types.md).
    
> [!NOTE]
> Ändern Sie niemals die **ADRLIST-Struktur,** die an **IABLogon::P repareRecips** übergeben wird, oder ändern Sie die Anzahl der Einträge. 
  
## <a name="see-also"></a>Siehe auch

- [ADRLIST](adrlist.md)
- [IMAPIProp::GetProps](imapiprop-getprops.md)
- [PidTagEntryId (kanonische Eigenschaft)](pidtagentryid-canonical-property.md)
- [SPropValue](spropvalue.md)
- [IABLogon : IUnknown](iablogoniunknown.md)

