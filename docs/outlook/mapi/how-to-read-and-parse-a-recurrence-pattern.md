---
title: Lesen und Analysieren eines Serienmusters
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
localization_priority: Normal
api_type:
- COM
ms.assetid: 75113097-b3ae-4d20-9796-85c62a592ef0
description: 'Letzte Änderung: Samstag, 23. Juli 2011'
ms.openlocfilehash: c226fe79fd002cda3c557fc8416c25f98ad33626
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 04/23/2019
ms.locfileid: "32345927"
---
# <a name="read-and-parse-a-recurrence-pattern"></a><span data-ttu-id="2e413-103">Lesen und Analysieren eines Serienmusters</span><span class="sxs-lookup"><span data-stu-id="2e413-103">Read and parse a recurrence pattern</span></span>
  
<span data-ttu-id="2e413-104">**Gilt für**: Outlook 2013 | Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="2e413-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
<span data-ttu-id="2e413-105">MAPI kann zum Lesen und Analysieren eines Serienmusters für einen Termin verwendet werden.</span><span class="sxs-lookup"><span data-stu-id="2e413-105">MAPI can be used to read and parse a recurrence pattern for an appointment.</span></span>
  
<span data-ttu-id="2e413-106">Informationen zum herunterladen, anzeigen und Ausführen des Codes aus dem MFCMAPI-Anwendungsprojekt, auf das in diesem Thema verwiesen wird, finden Sie unter [Installieren der in diesem Abschnitt verwendeten Beispiele](how-to-install-the-samples-used-in-this-section.md).</span><span class="sxs-lookup"><span data-stu-id="2e413-106">For information about how to download, view, and run the code from the MFCMAPI application project referenced in this topic, see [Install the Samples Used in This Section](how-to-install-the-samples-used-in-this-section.md).</span></span>

### <a name="to-parse-a-recurrence-blob"></a><span data-ttu-id="2e413-107">So analysieren Sie einen Serien-BLOB</span><span class="sxs-lookup"><span data-stu-id="2e413-107">To parse a recurrence blob</span></span>

1. <span data-ttu-id="2e413-108">Öffnen Sie ein Terminelement.</span><span class="sxs-lookup"><span data-stu-id="2e413-108">Open an appointment item.</span></span> <span data-ttu-id="2e413-109">Informationen zum Öffnen einer Nachricht finden Sie unter [Öffnen einer Nachricht](opening-a-message.md).</span><span class="sxs-lookup"><span data-stu-id="2e413-109">For information about opening a message, see [Opening a Message](opening-a-message.md).</span></span>
    
2. <span data-ttu-id="2e413-110">Rufen Sie die benannte Eigenschaft **dispidApptRecur** ([Pidlidappointmentrecur (kanonische Eigenschaft](pidlidappointmentrecur-canonical-property.md)) ab.</span><span class="sxs-lookup"><span data-stu-id="2e413-110">Retrieve the named property **dispidApptRecur** ([PidLidAppointmentRecur Canonical Property](pidlidappointmentrecur-canonical-property.md)).</span></span> <span data-ttu-id="2e413-111">Informationen zum Abrufen benannter Eigenschaften finden Sie unter [MAPI Named Properties](mapi-named-properties.md).</span><span class="sxs-lookup"><span data-stu-id="2e413-111">For information about retrieving named properties, see [MAPI Named Properties](mapi-named-properties.md).</span></span>
    
3. <span data-ttu-id="2e413-112">Folgen Sie den Anweisungen in [[MS-OXOCAL]](https://msdn.microsoft.com/library/cc425490%28EXCHG.80%29.aspx) , um die Struktur des Terminserien Musters zu lesen.</span><span class="sxs-lookup"><span data-stu-id="2e413-112">Follow the guidance in [[MS-OXOCAL]](https://msdn.microsoft.com/library/cc425490%28EXCHG.80%29.aspx) to read the appointment recurrence pattern structure.</span></span> 
    
<span data-ttu-id="2e413-113">Die MFCMAPI-Referenzanwendung demonstriert den letzten Schritt mit `BinToAppointmentRecurrencePatternStruct` der Funktion in der InterpretProp2. cpp-Quelldatei des MfcMapi-Projekts.</span><span class="sxs-lookup"><span data-stu-id="2e413-113">The MFCMAPI reference application demonstrates the last step with the  `BinToAppointmentRecurrencePatternStruct` function in the InterpretProp2.cpp source file of the MFCMapi project.</span></span> <span data-ttu-id="2e413-114">Die `BinToAppointmentRecurrencePatternStruct` Funktion verwendet einen Zeiger auf einen Puffer im Arbeitsspeicher als Parameter.</span><span class="sxs-lookup"><span data-stu-id="2e413-114">The  `BinToAppointmentRecurrencePatternStruct` function takes a pointer to a buffer in memory as a parameter.</span></span> <span data-ttu-id="2e413-115">Die MFCMAPI-Anwendung ruft diesen Puffer ab, indem zunächst die benannte Eigenschaft **dispidApptRecur** einem Property-Tag zugeordnet und dann der Wert der Eigenschaft mithilfe der [IMAPIProp::](imapiprop-getprops.md) GetProps-Methode angefordert wird.</span><span class="sxs-lookup"><span data-stu-id="2e413-115">The MFCMAPI application obtains this buffer by first mapping the **dispidApptRecur** named property to a property tag, then by requesting the property's value using the [IMAPIProp::GetProps](imapiprop-getprops.md) method.</span></span> <span data-ttu-id="2e413-116">Wenn die Eigenschaft zu umfangreich ist, um Sie \*\*\*\* mit der GetProps-Methode abzurufen, öffnet MfcMapi eine Stream-Schnittstelle zum Abrufen der Eigenschaft mithilfe der [IMAPIProp:: OpenProperty](imapiprop-openproperty.md) -Methode.</span><span class="sxs-lookup"><span data-stu-id="2e413-116">If the property is too large to retrieve using the **GetProps** method, MFCMAPI opens a stream interface to retrieve the property using the [IMAPIProp::OpenProperty](imapiprop-openproperty.md) method.</span></span> <span data-ttu-id="2e413-117">Die MFCMAPI-Anwendung liest dann die Daten aus dem Stream, um den Puffer zu erstellen.</span><span class="sxs-lookup"><span data-stu-id="2e413-117">The MFCMAPI application then reads the data out of the stream to build the buffer.</span></span> 
  
<span data-ttu-id="2e413-118">Informationen zum Format des Puffers finden Sie unter der [kanonischEn Eigenschaft pidlidappointmentrecur (](pidlidappointmentrecur-canonical-property.md).</span><span class="sxs-lookup"><span data-stu-id="2e413-118">For information about the format of the buffer, see the [PidLidAppointmentRecur Canonical Property](pidlidappointmentrecur-canonical-property.md).</span></span> <span data-ttu-id="2e413-119">Der größte Teil der Daten im Puffer besteht aus Feldern mit einer festen Anzahl von Bytes, die nacheinander gelesen werden müssen.</span><span class="sxs-lookup"><span data-stu-id="2e413-119">The bulk of the data in the buffer consists of fields of a fixed number of bytes, which must be read one after another.</span></span> <span data-ttu-id="2e413-120">Einige Felder sind nur vorhanden, wenn andere Felder bestimmte Werte enthalten, und die Größe einiger Felder hängt möglicherweise vom Wert anderer Felder ab.</span><span class="sxs-lookup"><span data-stu-id="2e413-120">Some fields are present only if other fields contain certain values, and the size of some fields may depend on the value of other fields.</span></span> <span data-ttu-id="2e413-121">Das Analysieren des Puffers zum Lesen der verschiedenen Felder erfordert viel Buchhaltung.</span><span class="sxs-lookup"><span data-stu-id="2e413-121">Parsing the buffer to read the various fields involves a lot of bookkeeping.</span></span> <span data-ttu-id="2e413-122">MFCMAPI verwendet eine interne Hilfsklasse namens `CBinaryParser` zum Kapseln dieser Buchhaltung.</span><span class="sxs-lookup"><span data-stu-id="2e413-122">MFCMAPI uses an internal helper class named  `CBinaryParser` to encapsulate this bookkeeping.</span></span> <span data-ttu-id="2e413-123">Die `CBinaryParser::GetDWORD` -Funktion überprüft beispielsweise, ob genügend Bytes im Puffer verbleiben, um einen DWORD-Wert zu lesen, und liest dann den Value und aktualisiert die Zeiger.</span><span class="sxs-lookup"><span data-stu-id="2e413-123">For example, the  `CBinaryParser::GetDWORD` function checks whether enough bytes remain in the buffer to read a DWORD, and then reads the value and updates the pointers.</span></span> 
  
<span data-ttu-id="2e413-124">Nachdem der Puffer in eine Struktur analysiert wurde, verwendet die MFCMAPI-Anwendung die `AppointmentRecurrencePatternStructToString` -Funktion, um die Struktur in eine Zeichenfolge umzuwandeln, die dem Benutzer angezeigt wird.</span><span class="sxs-lookup"><span data-stu-id="2e413-124">After the buffer has been parsed into a structure, the MFCMAPI application uses the  `AppointmentRecurrencePatternStructToString` function to convert the structure to a string to display to the user.</span></span> <span data-ttu-id="2e413-125">Dabei handelt es sich nicht um dieselbe Zeichenfolge, die Outlook anzeigen würde, sondern stattdessen eine RAW-Ansicht der Daten, bei denen Outlook Ihre Logik erstellt.</span><span class="sxs-lookup"><span data-stu-id="2e413-125">This is not the same string Outlook would display, but is instead a raw view of the data upon which Outlook builds its logic.</span></span> 
  
<span data-ttu-id="2e413-126">Es kann ein Puffer auftreten, der entweder beschädigte Daten oder mehr Daten enthält, als zur Codierung eines Serienmusters erforderlich ist.</span><span class="sxs-lookup"><span data-stu-id="2e413-126">It is possible to encounter a buffer which contains either corrupted data or more data than is needed to encode a recurrence pattern.</span></span> <span data-ttu-id="2e413-127">Um diese Szenarien zu identifizieren, verfolgt die MFCMAPI-Anwendung, wie viele Daten erfolgreich analysiert wurden und wie viel im Puffer verbleiben.</span><span class="sxs-lookup"><span data-stu-id="2e413-127">To help identify those scenarios, the MFCMAPI application keeps track of how much data has been successfully parsed and how much remains in the buffer.</span></span> <span data-ttu-id="2e413-128">Wenn die Daten nach Abschluss der Analyse im Puffer bleiben, enthält MFCMAPI diese "Junk-Daten" in der Struktur, damit Sie untersucht werden können.</span><span class="sxs-lookup"><span data-stu-id="2e413-128">If data remains in the buffer after parsing has completed, MFCMAPI includes this "junk data" in the structure so it can be examined.</span></span>
  
<span data-ttu-id="2e413-129">Nachfolgend finden Sie eine vollständige Liste `BinToAppointmentRecurrencePatternStruct` der Funktionen.</span><span class="sxs-lookup"><span data-stu-id="2e413-129">The following is the complete listing of the  `BinToAppointmentRecurrencePatternStruct` function.</span></span> 
  
```cpp
AppointmentRecurrencePatternStruct* BinToAppointmentRecurrencePatternStruct(ULONG cbBin, LPBYTE lpBin)
{
   if (!lpBin) return NULL;
   AppointmentRecurrencePatternStruct arpPattern = {0};
   CBinaryParser Parser(cbBin,lpBin);
   size_t cbBinRead = 0;
   arpPattern.RecurrencePattern = BinToRecurrencePatternStruct(cbBin,lpBin,&cbBinRead);
   Parser.Advance(cbBinRead);
   Parser.GetDWORD(&arpPattern.ReaderVersion2);
   Parser.GetDWORD(&arpPattern.WriterVersion2);
   Parser.GetDWORD(&arpPattern.StartTimeOffset);
   Parser.GetDWORD(&arpPattern.EndTimeOffset);
   Parser.GetWORD(&arpPattern.ExceptionCount);
   if (arpPattern.ExceptionCount &&
      arpPattern.ExceptionCount == arpPattern.RecurrencePattern->ModifiedInstanceCount &&
      arpPattern.ExceptionCount < _MaxExceptions)
   {
      arpPattern.ExceptionInfo = new ExceptionInfoStruct[arpPattern.ExceptionCount];
      if (arpPattern.ExceptionInfo)
      {
         memset(arpPattern.ExceptionInfo,0,sizeof(ExceptionInfoStruct) * arpPattern.ExceptionCount);
         WORD i = 0;
         for (i = 0 ; i < arpPattern.ExceptionCount ; i++)
         {
            Parser.GetDWORD(&arpPattern.ExceptionInfo[i].StartDateTime);
            Parser.GetDWORD(&arpPattern.ExceptionInfo[i].EndDateTime);
            Parser.GetDWORD(&arpPattern.ExceptionInfo[i].OriginalStartDate);
            Parser.GetWORD(&arpPattern.ExceptionInfo[i].OverrideFlags);
            if (arpPattern.ExceptionInfo[i].OverrideFlags & ARO_SUBJECT)
            {
               Parser.GetWORD(&arpPattern.ExceptionInfo[i].SubjectLength);
               Parser.GetWORD(&arpPattern.ExceptionInfo[i].SubjectLength2);
               if (arpPattern.ExceptionInfo[i].SubjectLength2 && arpPattern.ExceptionInfo[i].SubjectLength2 + 1 
                  == arpPattern.ExceptionInfo[i].SubjectLength)
               {
                  Parser.GetStringA(arpPattern.ExceptionInfo[i].SubjectLength2,&arpPattern.ExceptionInfo[i].Subject);
               }
            }
            if (arpPattern.ExceptionInfo[i].OverrideFlags & ARO_MEETINGTYPE)
            {
               Parser.GetDWORD(&arpPattern.ExceptionInfo[i].MeetingType);
            }
            if (arpPattern.ExceptionInfo[i].OverrideFlags & ARO_REMINDERDELTA)
            {
               Parser.GetDWORD(&arpPattern.ExceptionInfo[i].ReminderDelta);
            }
            if (arpPattern.ExceptionInfo[i].OverrideFlags & ARO_REMINDER)
            {
               Parser.GetDWORD(&arpPattern.ExceptionInfo[i].ReminderSet);
            }
            if (arpPattern.ExceptionInfo[i].OverrideFlags & ARO_LOCATION)
            {
               Parser.GetWORD(&arpPattern.ExceptionInfo[i].LocationLength);
               Parser.GetWORD(&arpPattern.ExceptionInfo[i].LocationLength2);
               if (arpPattern.ExceptionInfo[i].LocationLength2 && arpPattern.ExceptionInfo[i].LocationLength2 
                  + 1 == arpPattern.ExceptionInfo[i].LocationLength)
               {
                  Parser.GetStringA(arpPattern.ExceptionInfo[i].LocationLength2,&arpPattern.ExceptionInfo[i].Location);
               }
            }
            if (arpPattern.ExceptionInfo[i].OverrideFlags & ARO_BUSYSTATUS)
            {
               Parser.GetDWORD(&arpPattern.ExceptionInfo[i].BusyStatus);
            }
            if (arpPattern.ExceptionInfo[i].OverrideFlags & ARO_ATTACHMENT)
            {
               Parser.GetDWORD(&arpPattern.ExceptionInfo[i].Attachment);
            }
            if (arpPattern.ExceptionInfo[i].OverrideFlags & ARO_SUBTYPE)
            {
               Parser.GetDWORD(&arpPattern.ExceptionInfo[i].SubType);
            }
            if (arpPattern.ExceptionInfo[i].OverrideFlags & ARO_APPTCOLOR)
            {
               Parser.GetDWORD(&arpPattern.ExceptionInfo[i].AppointmentColor);
            }
         }
      }
   }
   Parser.GetDWORD(&arpPattern.ReservedBlock1Size);
   if (arpPattern.ReservedBlock1Size && arpPattern.ReservedBlock1Size < _MaxReservedBlock)
   {
      Parser.GetBYTES(arpPattern.ReservedBlock1Size,&arpPattern.ReservedBlock1);
   }
   if (arpPattern.ExceptionCount &&
      arpPattern.ExceptionCount == arpPattern.RecurrencePattern->ModifiedInstanceCount &&
      arpPattern.ExceptionCount < _MaxExceptions &&
      arpPattern.ExceptionInfo)
   {
      arpPattern.ExtendedException = new ExtendedExceptionStruct[arpPattern.ExceptionCount];
      if (arpPattern.ExtendedException)
      {
         memset(arpPattern.ExtendedException,0,sizeof(ExtendedExceptionStruct) * arpPattern.ExceptionCount);
         WORD i = 0;
         for (i = 0 ; i < arpPattern.ExceptionCount ; i++)
         {
            if (arpPattern.WriterVersion2 >= 0x0003009)
            {
               Parser.GetDWORD(&arpPattern.ExtendedException[i].ChangeHighlight.ChangeHighlightSize);
               Parser.GetDWORD(&arpPattern.ExtendedException[i].ChangeHighlight.ChangeHighlightValue);
               if (arpPattern.ExtendedException[i].ChangeHighlight.ChangeHighlightSize > sizeof(DWORD))
               {
                  Parser.GetBYTES(arpPattern.ExtendedException[i].ChangeHighlight.ChangeHighlightSize 
                     - sizeof(DWORD),&arpPattern.ExtendedException[i].ChangeHighlight.Reserved);
               }
            }
            Parser.GetDWORD(&arpPattern.ExtendedException[i].ReservedBlockEE1Size);
            if (arpPattern.ExtendedException[i].ReservedBlockEE1Size &&
                arpPattern.ExtendedException[i].ReservedBlockEE1Size < _MaxReservedBlock)
            {
               Parser.GetBYTES(arpPattern.ExtendedException[i].ReservedBlockEE1Size,&arpPattern.ExtendedException[i].ReservedBlockEE1);
            }
            if (arpPattern.ExceptionInfo[i].OverrideFlags & ARO_SUBJECT ||
               arpPattern.ExceptionInfo[i].OverrideFlags & ARO_LOCATION)
            {
               Parser.GetDWORD(&arpPattern.ExtendedException[i].StartDateTime);
               Parser.GetDWORD(&arpPattern.ExtendedException[i].EndDateTime);
               Parser.GetDWORD(&arpPattern.ExtendedException[i].OriginalStartDate);
            }
            if (arpPattern.ExceptionInfo[i].OverrideFlags & ARO_SUBJECT)
            {
               Parser.GetWORD(&arpPattern.ExtendedException[i].WideCharSubjectLength);
               if (arpPattern.ExtendedException[i].WideCharSubjectLength)
               {
                  Parser.GetStringW(arpPattern.ExtendedException[i].WideCharSubjectLength,&arpPattern.ExtendedException[i].WideCharSubject);
               }
            }
            if (arpPattern.ExceptionInfo[i].OverrideFlags & ARO_LOCATION)
            {
               Parser.GetWORD(&arpPattern.ExtendedException[i].WideCharLocationLength);
               if (arpPattern.ExtendedException[i].WideCharLocationLength)
               {
                  Parser.GetStringW(arpPattern.ExtendedException[i].WideCharLocationLength,&arpPattern.ExtendedException[i].WideCharLocation);
               }
            }
            if (arpPattern.ExceptionInfo[i].OverrideFlags & ARO_SUBJECT ||
               arpPattern.ExceptionInfo[i].OverrideFlags & ARO_LOCATION)
            {
               Parser.GetDWORD(&arpPattern.ExtendedException[i].ReservedBlockEE2Size);
               if (arpPattern.ExtendedException[i].ReservedBlockEE2Size && arpPattern.ExtendedException[i].ReservedBlockEE2Size < _MaxReservedBlock)
               {
                  Parser.GetBYTES(arpPattern.ExtendedException[i].ReservedBlockEE2Size,&arpPattern.ExtendedException[i].ReservedBlockEE2);
               }
            }
         }
      }
   }
   Parser.GetDWORD(&arpPattern.ReservedBlock2Size);
   if (arpPattern.ReservedBlock2Size && arpPattern.ReservedBlock2Size < _MaxReservedBlock)
   {
      Parser.GetBYTES(arpPattern.ReservedBlock2Size,&arpPattern.ReservedBlock2);
   }
   // Junk data remains.
   if (Parser.RemainingBytes() > 0)
   {
      arpPattern.JunkDataSize = Parser.RemainingBytes();
      Parser.GetBYTES(arpPattern.JunkDataSize,&arpPattern.JunkData);
   }
   AppointmentRecurrencePatternStruct* parpPattern = new AppointmentRecurrencePatternStruct;
   if (parpPattern)
   {
      *parpPattern = arpPattern;
   }
   return parpPattern;
}

```

## <a name="see-also"></a><span data-ttu-id="2e413-130">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="2e413-130">See also</span></span>

- [<span data-ttu-id="2e413-131">Verwenden von MAPI zum Erstellen von Outlook 2007-Elementen</span><span class="sxs-lookup"><span data-stu-id="2e413-131">Using MAPI to Create Outlook 2007 Items</span></span>](https://msdn.microsoft.com/library/cc678348%28office.12%29.aspx)

