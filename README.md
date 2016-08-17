# NotesApplication
A note application for taking notes
/*A Note Application Class*/
class NotesApplication{
    
	//initialize object
	constructor(author){
		this.author = author;
		this.notes = [];
	}
	
	create(note_content){
		this.notes.push(note_content);
	}
	
	listNotes(){
		var list = ""
		for( var i = 0; i < this.notes.length; i++ ){
			list += "Note ID: " + i + "\n";
			list += this.notes[i] + "\n\n";
			list += "By Author " + this.author + "\n\n";
		}
		console.log(list);
	}
	
	get(note_id){
		return this.notes[note_id];
	}
	
	search(search_text){
		var list = "Showing results for search ‘" + search_text + "’" + "\n\n";
		
		for( var i = 0; i < this.notes.length; i++ ){
			
			if(this.notes[i].includes(search_text)){
			list += "Note ID: " + i + "\n";
			list += this.notes[i] + "\n\n";
			list += "By Author " + this.author + "\n\n";
			}
		}
		
		return list;
	}
}