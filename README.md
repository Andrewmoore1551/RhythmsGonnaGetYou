# RhythmsGonnaGetYou

Problem

- We are starting a record label company named ”Record Company Name”. We need to create an app that stores our bands,albums and songs data.

C R U D

- Create: Create Albums, Songs, & Bands
- Read: View the Bands, Albums, and Albums of Specific Bands
- Update: Release a Band from Contract and Resign a Band
- Delete: Not Deleting any information from the Database

EXAMPLES
Jams has released Artist Clutch from their 4 yr contract.
Jams signed The Killers, they have 6 albums.
View a list of all of Jams Albums.
Clutch added a digital release of Track 4 on the Album Elephant Riders
Black Flags discography.
Artist 7 Seconds has signed with Jams.
7 Seconds has 11 Albums with a total of 96 Tracks.

Data Structure:

- Create classes called:

- Bands
  Properties
  ID INTEGER
  BandName TEXT
  CountryOfOrigin TEXT
  NumberOfMembers INTEGER
  Website TEXT
  Style TEXT
  IsSigned Boolean
  ContactName TEXT
  ContactPhone INTEGER

Albums
ID INTEGER
Title TEXT
IsExplicit BOOLEAN
ReleaseDate DATE
BandId INTEGER

- Songs
  Id INTEGER
  TrackNumber INTEGER
  Title TEXT
  Duration INTEGER (Time?)
  AlbumId INTEGER
- Context
  DbContext Class

Algorithm

SQL Commands
Create a database of existing Bands, Albums and Songs
This will be 3 tables
Bands
Albums
Join BandId to Albums
BandID=INTEGER REFERENCES “Bands”(“Id”)
Songs that share the above class properties.
Join AlbumId to Songs
AlbumId=INTEGER REFERENCES “Albums”(“Id”)
Populate the Tables with data

C# Algorithm
Welcome to the app
Console.WriteLine(message)

Create Class Artists/Bands
Properties:
ID INTEGER - public int Id {get; set;}
Name TEXT - public string Name {get; set;}
CountryOfOrigin TEXT - public string CountryOfOrigin {get; set;}
NumberOfMembers INTEGER - public int NumberOfMembers {get; set;}
Website TEXT - public string Website {get; set;}
Style TEXT - public string Style {get; set;}
IsSigned Boolean - public bool IsSigned {get; set;}
ContactName TEXT - public string ContactName {get; set;}
ContactNumber TEXT - public int ContactNumber {get; set;}

Create Class Albums
Properties:
ID INTEGER - public int Id {get; set;}
Title TEXT - public string Title {get; set;}
IsExplicit BOOLEAN - public bool IsExplicit {get; set;}
ReleaseDate DATE - public DateTime ReleaseDate {get; set;}
BandId - public BandId { get; set; }

// Public int BandId {get; set; } /do after DBContext Class is created
// Public Bands Band {get; set; } /do after DBContext Class is created

Create Class Songs
Properties:
Id INTEGER - public int Id {get; set;}
TrackNumber INTEGER - public int TrackNumber {get; set;}
Title TEXT - public string Title {get; set;}
Duration INTEGER (Time?) - public int
AlbumId INTEGER -

Create Class DBContext
Property:

//dotnet add package Npgsql.EntityFrameworkCore.PostgreSQL

Public DBset<Band> Bands {get; set;}
Public DBSET<Album> Albums {get; set;)

Display the Menu Options(Tons of Different options):
Band - Album - Song - View - Quit

    While the User hasn’t chosen to QUIT: (Bool is false)

Writeline “Please choose from the following:”
CW: Bands/Artists - View all artists/bands, sign a band, release a band,
CW: Albums - View all albums (by release date), Add an Album
Prompt for a band name and view all their albums
CW: Songs - Add a new song to an album
CW: View - Bands that are signed or unsigned.
CW: Quit
CW:Please choose
CR:();
Var choice = CR()
Make ToLower(). Trim();

If (choice = “bands”)

CW(“Would you like to (s)ign, (r)elease or (v)iew all bands)
Var userChoice = CR();

If (userChoice = “s”)
{
//how to add/sign bands
var newBand = new Band {
BandName = "The Boogers",
CountryOfOrigin = "US",
NumberOfMembers = 3,
Website = “theboogers.com”,
Style = “Punk”,
ContactName = “Joe Booger”,
ContactNumber = 7654
};
context.Bands.Add(newBand);
context.SaveChanges();
}
If (userChoice = “r”)
{
//how to delete/release bands
var existingBand = context.Bands.FirstOrDefault(band => band.BandName == "The Boogers");
(inside remove if) if (existingBand != null) {
context.Bands.Remove(existingBand);
context.SaveChanges();
}

If (userChoice = “v”)//view all bands
foreach (var band in Bands)
{
Console.WriteLine($"Our list of bands is {bands.Name}");
}

If (choice = “Album”)
CW(“(A)dd an Album, (V)iew albums by release date,(S)ee all albums from a band”);

var albumChoice = CRL();
var = Console.ReadLine();
string v = choice.ToUpper().Trim();
choice = v;

if (albumChoice = “A”)
{
var newAlbum = new Album {
Title = "The Shit",
IsExplicit = True,
ReleaseDate = 1989-01-23,
BandId = 2
};
If (albumChoice = “V”)
albums.OrderBy(albumsReleaseDate => albumsReleaseDate.ReleaseDate);
CWL();
CWL(“Here is your list”);
//created var for album in albums
Foreach (var album in albums)
{ //will show album title and release date.
CWL($” {album.Title} {album.ReleaseDate}”);
}
}

If (albumChoice = ”S”)
{
console.WL(“Which bands discography would you like to see?”);
Var usersBandChoice= Console.Readline();

}
//im looking at ERD // this is version 1
context.Bands.Where(band => band.name == myReadLineVariableHere)
Include(..Album..)
//version two
Var band = context.Bands.FirstorDefault (search for that band by name)
Var foundBandId = band.Id
context.Album.Where( the album has the band id we care about)

Style = “Punk”,
ContactName = “Joe Booger”,
ContactNumber = 8131234321
};

If (choice = “Songs”)
Var newSong = new Songs {
TrackNumber =
Title =
Duration =
AlbumbId =
};

If (choice=”View”)
Ask what they would like to view.
CWL(“Here are your options:\n 1. by release View albumsdate \n 2. All Bands \n3. View bands that are Signed. \n4. (V)iew bands that are unsigned. \n 5. Enter a band name to view their albums. ~Please enter a number~
CR(); //1-5//
If (choice = 1)
{Console.WriteLine($"There is a Album named {album.Title} that was released on {album.ReleaseDate}");
}
If choice

//view band example

//example
Var userChoice = Console.ReadLine();
Var userInput = int.Parse(userchoice);
// example of order by release date
albums.Orderby(albumDate => albumDate.ReleaseDate);

If(choice=”Albums”)
CR():

View albums by release date?

If (choice = ”Bands”
CR():
CW(“Which band would you like to see?”);
CR():
//dirty bhole == “BandId” => 1
If (choice =
Enter “band name” to view all their albums?

“ArtistId”

//for viewing unsigned artist
foreach (var artist in artists)
{
If (artist.IsSigned == False)
{
CW($”{artist.IsSigned} - is unsigned);
}
