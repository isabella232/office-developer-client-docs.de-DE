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
ms.openlocfilehash: 694d63165bb820ffef1a29d1646861435fc4ed26
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 06/11/2018
ms.locfileid: "19791870"
---
# <a name="read-and-parse-a-recurrence-pattern"></a><span data-ttu-id="93ea0-103">Lesen und Analysieren eines Serienmusters</span><span class="sxs-lookup"><span data-stu-id="93ea0-103">Read and parse a recurrence pattern</span></span>
  
<span data-ttu-id="93ea0-104">**Betrifft**: Outlook</span><span class="sxs-lookup"><span data-stu-id="93ea0-104">**Applies to**: Outlook</span></span> 
  
<span data-ttu-id="93ea0-105">MAPI kann zum Lesen und Analysieren eines Serienmusters, das für einen Termin verwendet werden.</span><span class="sxs-lookup"><span data-stu-id="93ea0-105">MAPI can be used to read and parse a recurrence pattern for an appointment.</span></span>
  
<span data-ttu-id="93ea0-106">Informationen zum Herunterladen, anzeigen, und führen Sie den Code aus dem MFCMAPI (engl.) Anwendung-Projekt verwiesen, die in diesem Thema finden Sie unter [Installieren der Beispiele in diesem Abschnitt verwendet](how-to-install-the-samples-used-in-this-section.md).</span><span class="sxs-lookup"><span data-stu-id="93ea0-106">For information about how to download, view, and run the code from the MFCMAPI application project referenced in this topic, see [Install the Samples Used in This Section](how-to-install-the-samples-used-in-this-section.md).</span></span>

### <a name="to-parse-a-recurrence-blob"></a><span data-ttu-id="93ea0-107">Analysieren einen Serienblob</span><span class="sxs-lookup"><span data-stu-id="93ea0-107">To parse a recurrence blob</span></span>

1. <span data-ttu-id="93ea0-108">Öffnen Sie ein Terminelement.</span><span class="sxs-lookup"><span data-stu-id="93ea0-108">Open an appointment item.</span></span> <span data-ttu-id="93ea0-109">Informationen zum Öffnen einer Nachricht finden Sie unter [Öffnen einer Nachricht](opening-a-message.md).</span><span class="sxs-lookup"><span data-stu-id="93ea0-109">For information about opening a message, see [Opening a Message](opening-a-message.md).</span></span>
    
2. <span data-ttu-id="93ea0-110">Rufen Sie die benannte Eigenschaft **DispidApptRecur** ([PidLidAppointmentRecur kanonische-Eigenschaft](pidlidappointmentrecur-canonical-property.md)) ab.</span><span class="sxs-lookup"><span data-stu-id="93ea0-110">Retrieve the named property **dispidApptRecur** ([PidLidAppointmentRecur Canonical Property](pidlidappointmentrecur-canonical-property.md)).</span></span> <span data-ttu-id="93ea0-111">Informationen zum Abrufen von benannten Eigenschaften finden Sie unter [MAPI-Eigenschaften mit dem Namen](mapi-named-properties.md).</span><span class="sxs-lookup"><span data-stu-id="93ea0-111">For information about retrieving named properties, see [MAPI Named Properties](mapi-named-properties.md).</span></span>
    
3. <span data-ttu-id="93ea0-112">Führen Sie die Anweisungen in [[MS-OXOCAL]](http://msdn.microsoft.com/de-de/library/cc425490%28EXCHG.80%29.aspx) die Termin Serie Muster-Struktur zu lesen.</span><span class="sxs-lookup"><span data-stu-id="93ea0-112">Follow the guidance in [[MS-OXOCAL]](http://msdn.microsoft.com/de-de/library/cc425490%28EXCHG.80%29.aspx) to read the appointment recurrence pattern structure.</span></span> 
    
<span data-ttu-id="93ea0-113">Die MFCMAPI (engl.)-Referenz-Anwendung veranschaulicht den letzten Schritt mit der `BinToAppointmentRecurrencePatternStruct` Funktion in der Quelldatei InterpretProp2.cpp des Projekts MFCMAPI (engl.).</span><span class="sxs-lookup"><span data-stu-id="93ea0-113">The MFCMAPI reference application demonstrates the last step with the  `BinToAppointmentRecurrencePatternStruct` function in the InterpretProp2.cpp source file of the MFCMapi project.</span></span> <span data-ttu-id="93ea0-114">Die `BinToAppointmentRecurrencePatternStruct` Funktion einen Zeiger auf einem Puffer im Arbeitsspeicher als Parameter akzeptiert.</span><span class="sxs-lookup"><span data-stu-id="93ea0-114">The  `BinToAppointmentRecurrencePatternStruct` function takes a pointer to a buffer in memory as a parameter.</span></span> <span data-ttu-id="93ea0-115">Die Anwendung MFCMAPI (engl.) abruft dieses Puffers durch Zuordnen von der **DispidApptRecur** -Eigenschaft auf ein Eigenschaftentag klicken Sie dann mit der durch den Wert der Eigenschaft mithilfe der Methode [IMAPIProp::GetProps](imapiprop-getprops.md) anfordern.</span><span class="sxs-lookup"><span data-stu-id="93ea0-115">The MFCMAPI application obtains this buffer by first mapping the **dispidApptRecur** named property to a property tag, then by requesting the property's value using the [IMAPIProp::GetProps](imapiprop-getprops.md) method.</span></span> <span data-ttu-id="93ea0-116">Wenn die Eigenschaft rufen Sie mithilfe der Methode **GetProps** zu groß ist, wird MFCMAPI (engl.) eine Stream-Schnittstelle zum Abrufen der Eigenschaft mithilfe der Methode [IMAPIProp::OpenProperty](imapiprop-openproperty.md) geöffnet.</span><span class="sxs-lookup"><span data-stu-id="93ea0-116">If the property is too large to retrieve using the **GetProps** method, MFCMAPI opens a stream interface to retrieve the property using the [IMAPIProp::OpenProperty](imapiprop-openproperty.md) method.</span></span> <span data-ttu-id="93ea0-117">Klicken Sie dann die MFCMAPI (engl.) Anwendung liest die Daten aus dem Datenstrom Puffer zu erstellen.</span><span class="sxs-lookup"><span data-stu-id="93ea0-117">The MFCMAPI application then reads the data out of the stream to build the buffer.</span></span> 
  
<span data-ttu-id="93ea0-118">Informationen über das Format des Puffers finden Sie unter der [PidLidAppointmentRecur kanonische-Eigenschaft](pidlidappointmentrecur-canonical-property.md).</span><span class="sxs-lookup"><span data-stu-id="93ea0-118">For information about the format of the buffer, see the [PidLidAppointmentRecur Canonical Property](pidlidappointmentrecur-canonical-property.md).</span></span> <span data-ttu-id="93ea0-119">Der Großteil der Daten im Puffer besteht aus Feldern eine festgelegte Anzahl von Bytes, die nach dem anderen gelesen werden muss.</span><span class="sxs-lookup"><span data-stu-id="93ea0-119">The bulk of the data in the buffer consists of fields of a fixed number of bytes, which must be read one after another.</span></span> <span data-ttu-id="93ea0-120">Einige Felder sind vorhanden, nur, wenn andere Felder bestimmte Werte enthalten, und die Größe der einige Felder kann der Wert der anderen Felder abhängen.</span><span class="sxs-lookup"><span data-stu-id="93ea0-120">Some fields are present only if other fields contain certain values, and the size of some fields may depend on the value of other fields.</span></span> <span data-ttu-id="93ea0-121">Analysieren den Puffer zum Lesen der verschiedenen Felder umfasst viele Buchhaltung.</span><span class="sxs-lookup"><span data-stu-id="93ea0-121">Parsing the buffer to read the various fields involves a lot of bookkeeping.</span></span> <span data-ttu-id="93ea0-122">MFCMAPI (engl.) verwendet wird, als interne Hilfsklasse, die mit dem Namen `CBinaryParser` dieser Buchhaltung kapseln.</span><span class="sxs-lookup"><span data-stu-id="93ea0-122">MFCMAPI uses an internal helper class named  `CBinaryParser` to encapsulate this bookkeeping.</span></span> <span data-ttu-id="93ea0-123">Beispielsweise die `CBinaryParser::GetDWORD` Funktion überprüft, ob genügend Bytes im Puffer zum Lesen von eines DWORD-Wert bleiben, und klicken Sie dann den Wert liest und die Zeiger aktualisiert.</span><span class="sxs-lookup"><span data-stu-id="93ea0-123">For example, the  `CBinaryParser::GetDWORD` function checks whether enough bytes remain in the buffer to read a DWORD, and then reads the value and updates the pointers.</span></span> 
  
<span data-ttu-id="93ea0-124">Nachdem Sie der Puffer in einer Struktur analysiert wurde, verwendet die Anwendung MFCMAPI (engl.) der `AppointmentRecurrencePatternStructToString` Funktion zum Konvertieren der Struktur in eine Zeichenfolge, die für den Benutzer anzuzeigen.</span><span class="sxs-lookup"><span data-stu-id="93ea0-124">After the buffer has been parsed into a structure, the MFCMAPI application uses the  `AppointmentRecurrencePatternStructToString` function to convert the structure to a string to display to the user.</span></span> <span data-ttu-id="93ea0-125">Dies ist nicht dieselbe Zeichenfolge, die Outlook angezeigt würden, die jedoch ist stattdessen eine unformatierte Ansicht der Daten auf denen Outlook seine Logik aufbaut.</span><span class="sxs-lookup"><span data-stu-id="93ea0-125">This is not the same string Outlook would display, but is instead a raw view of the data upon which Outlook builds its logic.</span></span> 
  
<span data-ttu-id="93ea0-126">Es ist möglich, einen Puffer auftreten, der beschädigte Daten oder mehr Daten als benötigt werden, um ein Serienmuster codieren enthält.</span><span class="sxs-lookup"><span data-stu-id="93ea0-126">It is possible to encounter a buffer which contains either corrupted data or more data than is needed to encode a recurrence pattern.</span></span> <span data-ttu-id="93ea0-127">Um diese Szenarien zu identifizieren, verfolgt die Anwendung MFCMAPI (engl.) über wie viele Daten erfolgreich analysiert wurde und wie viel im Puffer bleibt.</span><span class="sxs-lookup"><span data-stu-id="93ea0-127">To help identify those scenarios, the MFCMAPI application keeps track of how much data has been successfully parsed and how much remains in the buffer.</span></span> <span data-ttu-id="93ea0-128">Wenn Daten im Puffer bleibt, nachdem die Analyse abgeschlossen ist, einschließlich der MFCMAPI (engl.) dieses "Junk-e-Daten" in der Struktur, damit er untersucht werden kann.</span><span class="sxs-lookup"><span data-stu-id="93ea0-128">If data remains in the buffer after parsing has completed, MFCMAPI includes this "junk data" in the structure so it can be examined.</span></span>
  
<span data-ttu-id="93ea0-129">Im folgenden finden Sie eine vollständige Liste der der `BinToAppointmentRecurrencePatternStruct` Funktion.</span><span class="sxs-lookup"><span data-stu-id="93ea0-129">The following is the complete listing of the  `BinToAppointmentRecurrencePatternStruct` function.</span></span> 
  
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

## <a name="see-also"></a><span data-ttu-id="93ea0-130">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="93ea0-130">See also</span></span>

- [<span data-ttu-id="93ea0-131">Erstellen von Outlook 2007-Elementen mithilfe von MAPI</span><span class="sxs-lookup"><span data-stu-id="93ea0-131">Using MAPI to Create Outlook 2007 Items</span></span>](http://msdn.microsoft.com/de-de/library/cc678348%28office.12%29.aspx)

